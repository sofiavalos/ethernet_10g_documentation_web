---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-tx/"}
---

- **File**: [[10GBASE/MAC/eth_phy_10g_tx_code\|eth_phy_10g_tx_code]]

## Diagram
![Diagram](eth_phy_10g_tx.svg "Diagram")
## Hierarchical structure
![tx_compuesto.png](/img/user/10GBASE/PCS/tx_compuesto.png)
## Description

Modulo del transmisor de 10g
## Generics

| Generic name      | Type | Value          | Description                                                                 |
| ----------------- | ---- | -------------- | --------------------------------------------------------------------------- |
| DATA_WIDTH        |      | 64             | Ancho de datos                                                              |
| CTRL_WIDTH        |      | (DATA_WIDTH/8) | Ancho de control                                                            |
| HDR_WIDTH         |      | 2              | Ancho de header                                                             |
| BIT_REVERSE       |      | 0              | Flag que habilita la inversión de bits                                      |
| SCRAMBLER_DISABLE |      | 0              | Flag que habilita el scrambler                                              |
| PRBS31_ENABLE     |      | 0              | Flag que habilita la generacion de patrones pseudoaleatorios [[10GBASE/PCS/PRBS31\|PRBS31]]     |
| SERDES_PIPELINE   |      | 0              | Flag que habilita el uso de pipeline en el [[Abbreviations#SERDES\|SERDES]] |

## Ports

| Port name            | Direction | Type                  | Description                                                              |
| -------------------- | --------- | --------------------- | ------------------------------------------------------------------------ |
| clk                  | input     | wire                  | Señal de clock                                                           |
| rst                  | input     | wire                  | Señal de reset                                                           |
| xgmii_txc            | input     | wire [CTRL_WIDTH-1:0] | Señales de control de la interfaz [[Abbreviations#XGMII\|XGMII]]         |
| serdes_tx_data       | output    | wire [DATA_WIDTH-1:0] | Datos de salida para [[Abbreviations#SERDES\|SERDES]]                    |
| serdes_tx_hdr        | output    | wire [HDR_WIDTH-1:0]  | Header de salida para [[Abbreviations#SERDES\|SERDES]]                   |
| tx_bad_block         | output    | wire                  | Señal de estado para indicar un bloque defectuoso durante la transmisión |
| cfg_tx_prbs31_enable | input     | wire                  | Entrada para habilitar la generacion de patrones [[10GBASE/PCS/PRBS31\|PRBS31]]              |

## Signals

| Name            | Type                  | Description                      |
| --------------- | --------------------- | -------------------------------- |
| encoded_tx_data | wire [DATA_WIDTH-1:0] | Señal para datos codificados     |
| encoded_tx_hdr  | wire [HDR_WIDTH-1:0]  | Señal para encabezado codificado |

## Instantiations

- xgmii_baser_enc_inst: [[10GBASE/PCS/xgmii_baser_enc_64\|xgmii_baser_enc_64]]
  -  Instancia de modulo para la codificacion de datos segun estandar [[Abbreviations#XGMII\|XGMII]]
- eth_phy_10g_tx_if_inst: [[10GBASE/PCS/eth_phy_10g_tx_if\|eth_phy_10g_tx_if]]
  -  Instancia para la recepción de datos codificados desde la capa [[Abbreviations#XGMII\|XGMII]], la configuración de la transmisión según parámetros como el bit reverse, la habilitación o deshabilitación de scrambler y la generación de PRBS31, así como la transmisión de estos datos codificados y la configuración del [[Abbreviations#SERDES\|SERDES]]
