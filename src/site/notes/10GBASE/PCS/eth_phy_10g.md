---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g/"}
---


- **File**: [[10GBASE/PCS/eth_phy_10g_code\|eth_phy_10g_code]]

## Diagram
![Diagram](eth_phy_10g.svg "Diagram")
## Hierarchical structure
![modulo_completo_compuesto.png](/img/user/10GBASE/MAC/modulo_completo_compuesto.png)
## Generics

| Generic name        | Type | Value          | Description                                                                                                         |
| ------------------- | ---- | -------------- | ------------------------------------------------------------------------------------------------------------------- |
| DATA_WIDTH          |      | 64             | Ancho de bus de datos de 64 bits                                                                                    |
| CTRL_WIDTH          |      | (DATA_WIDTH/8) | Ancho de bus de control en bytes                                                                                    |
| HDR_WIDTH           |      | 2              | Ancho de header de sincronizacion (01 para bloques de data 10 para control), permiten establecer límites de bloques |
| BIT_REVERSE         |      | 0              | Flag para habilitar la inversión de bits                                                                            |
| SCRAMBLER_DISABLE   |      | 0              | Flag para habilitar el scrambler                                                                                    |
| PRBS31_ENABLE       |      | 0              | Flag para habilidar la secuencia pseudoaletoria [[10GBASE/PCS/PRBS31\|PRBS31]] para pruebas                                             |
| TX_SERDES_PIPELINE  |      | 0              | Flag para habilitar el pipeline en el transmisor                                                                    |
| RX_SERDES_PIPELINE  |      | 0              | Flag para habilitar el pipeline en el receptor                                                                      |
| BITSLIP_HIGH_CYCLES |      | 1              | Ciclos de bitslip bajos                                                                                             |
| BITSLIP_LOW_CYCLES  |      | 8              | Ciclos de bitslip altos                                                                                             |
| COUNT_125US         |      | 125000/6.4     | Contador de 125 us                                                                                                  |

## Ports

| Port name            | Direction | Type                  | Description                                                              |
| -------------------- | --------- | --------------------- | ------------------------------------------------------------------------ |
| rx_clk               | input     | wire                  | Señal de clock del receptor                                              |
| rx_rst               | input     | wire                  | Señal de reset del receptor                                              |
| tx_clk               | input     | wire                  | Señal de clock del transmisor                                            |
| tx_rst               | input     | wire                  | Señal de reset del transmisor                                            |
| xgmii_txd            | input     | wire [DATA_WIDTH-1:0] | Entrada para transmitir datos a la capa fisica                           |
| xgmii_txc            | input     | wire [CTRL_WIDTH-1:0] | Entrada para transmitir control a la capa fisica                         |
| xgmii_rxd            | output    | wire [DATA_WIDTH-1:0] | Salida para recibir datos de la capa fisica                              |
| xgmii_rxc            | output    | wire [CTRL_WIDTH-1:0] | Salida para recibir control de la capa fisica                            |
| serdes_tx_data       | output    | wire [DATA_WIDTH-1:0] | Salida para enviar datos serializados                                    |
| serdes_tx_hdr        | output    | wire [HDR_WIDTH-1:0]  | Salida para enviar encabezados serializados                              |
| serdes_rx_data       | input     | wire [DATA_WIDTH-1:0] | Entrada para recibir datos serializados                                  |
| serdes_rx_hdr        | input     | wire [HDR_WIDTH-1:0]  | Entrada para recibir encabezados serializados                            |
| serdes_rx_bitslip    | output    | wire                  | Señal de bitslip                                                         |
| serdes_rx_reset_req  | output    | wire                  | Señal de reset solicitado en el receptor                                 |
| tx_bad_block         | output    | wire                  | Señal de estado para indicar un bloque defectuoso durante la transmisión |
| rx_error_count       | output    | wire [6:0]            | Contador de errores del receptor                                         |
| rx_bad_block         | output    | wire                  | Señal de estado para indicar un bloque defectuoso durante la recepción   |
| rx_sequence_error    | output    | wire                  | Señal de error en la secuencia                                           |
| rx_block_lock        | output    | wire                  | Señal de bloque alineado                                                 |
| rx_high_ber          | output    | wire                  | Señal que indica un [[Abbreviations#BER\|BER]] alto                      |
| rx_status            | output    | wire                  | Señal que indica bloque alineado sin BER en 125us                        |
| cfg_tx_prbs31_enable | input     | wire                  | Señal que habilita [[10GBASE/PCS/PRBS31\|PRBS31]] en el transmisor                           |
| cfg_rx_prbs31_enable | input     | wire                  | Señal que habilita [[10GBASE/PCS/PRBS31\|PRBS31]] en el receptor                             |

## Instantiations

- eth_phy_10g_rx_inst: [[10GBASE/PCS/eth_phy_10g_rx\|eth_phy_10g_rx]]
  -  Modulo que coordina la decodificación de datos XGMII y gestiona la interfaz con el [[Abbreviations#SERDES\|SERDES]] del receptor.
- eth_phy_10g_tx_inst: [[10GBASE/PCS/eth_phy_10g_tx\|eth_phy_10g_tx]]
  -  Modulo que coordina la codificación de datos XGMII y gestiona la interfaz con el [[Abbreviations#SERDES\|SERDES]] de transmisión.
