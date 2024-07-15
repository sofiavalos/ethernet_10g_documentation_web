---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx/"}
---

- **File**: [[10GBASE/PCS/eth_phy_10g_rx_code\|eth_phy_10g_rx_code]]

## Diagram
![Diagram](eth_phy_10g_rx.svg "Diagram")
## Hierarchical structure
![rx_compuesto.png](/img/user/10GBASE/PCS/rx_compuesto.png)
## Description

Modulo del receptor de 10g

## Generics

| Generic name        | Type | Value          | Description                                  |
| ------------------- | ---- | -------------- | -------------------------------------------- |
| DATA_WIDTH          |      | 64             | Ancho del bus de datos                       |
| CTRL_WIDTH          |      | (DATA_WIDTH/8) | Ancho del bus de control                     |
| HDR_WIDTH           |      | 2              | Ancho de bus de header                       |
| BIT_REVERSE         |      | 0              | Flag para habilitar reversión de bits        |
| SCRAMBLER_DISABLE   |      | 0              | Flag para habilitar scrambler                |
| PRBS31_ENABLE       |      | 0              | Flag para habilitar [[10GBASE/PCS/PRBS31\|PRBS31]]               |
| SERDES_PIPELINE     |      | 0              | Flag para habilitar profundidad del pipeline |
| BITSLIP_HIGH_CYCLES |      | 1              | Ciclos de bitslip alto                       |
| BITSLIP_LOW_CYCLES  |      | 8              | Ciclos de bitslip bajo                       |
| COUNT_125US         |      | 125000/10      | Contador de 125 us                           |

## Ports

| Port name            | Direction | Type                  | Description                                                             |
| -------------------- | --------- | --------------------- | ----------------------------------------------------------------------- |
| clk                  | input     | wire                  | Señal de datos                                                          |
| rst                  | input     | wire                  | Señal de control                                                        |
| xgmii_rxd            | output    | wire [DATA_WIDTH-1:0] | Salida de datos de la interfaz [[Abbreviations#XGMII\|XGMII]]           |
| xgmii_rxc            | output    | wire [CTRL_WIDTH-1:0] | Salida de control de la interfaz [[Abbreviations#XGMII\|XGMII]]         |
| serdes_rx_data       | input     | wire [DATA_WIDTH-1:0] | Datos de la interfaz serdes del receptor                                |
| serdes_rx_hdr        | input     | wire [HDR_WIDTH-1:0]  | Sync eader de la interfaz [[Abbreviations#SERDES\|SERDES]] del receptor |
| serdes_rx_bitslip    | output    | wire                  | Flag de bitslip del [[Abbreviations#SERDES\|SERDES]]                    |
| serdes_rx_reset_req  | output    | wire                  | Flag de solicitud de reset del [[Abbreviations#SERDES\|SERDES]]         |
| rx_error_count       | output    | wire [6:0]            | Contador de errores                                                     |
| rx_bad_block         | output    | wire                  | Flag de bloque con error                                                |
| rx_sequence_error    | output    | wire                  | Flag de error de secuencia                                              |
| rx_block_lock        | output    | wire                  | Flag de bloque alineado                                                 |
| rx_high_ber          | output    | wire                  | Flag de bit rate error alto                                             |
| rx_status            | output    | wire                  | Flag del estado del receptor                                            |
| cfg_rx_prbs31_enable | input     | wire                  | Entrada para habilitar la [[10GBASE/PCS/PRBS31\|PRBS31]]                                    |

## Signals

| Name            | Type                  | Description                   |
| --------------- | --------------------- | ----------------------------- |
| encoded_rx_data | wire [DATA_WIDTH-1:0] | Datos codificados del rx      |
| encoded_rx_hdr  | wire [HDR_WIDTH-1:0]  | Sync header codificado del rx |

## Instantiations

- eth_phy_10g_rx_if_inst: [[10GBASE/PCS/eth_phy_10g_rx_if\|eth_phy_10g_rx_if]]
  -  Instancia modulo if del receptor que utiliza interfaz [[Abbreviations#SERDES\|SERDES]]
- xgmii_baser_dec_inst: [[10GBASE/PCS/xgmii_baser_dec_64\|xgmii_baser_dec_64]]
  -  Instancia modulo que convierte interfaz [[Abbreviations#XGMII\|XGMII]] a [[Abbreviations#SERDES\|SERDES]]
