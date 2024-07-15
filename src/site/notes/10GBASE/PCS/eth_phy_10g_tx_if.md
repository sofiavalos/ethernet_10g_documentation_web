---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-tx-if/"}
---

- **File**: [[10GBASE/MAC/eth_phy_10g_tx_if_code\|eth_phy_10g_tx_if_code]]

## Diagram
![Diagram](eth_phy_10g_tx_if.svg "Diagram")
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

| Port name            | Direction | Type                  | Description                                                       |
| -------------------- | --------- | --------------------- | ----------------------------------------------------------------- |
| clk                  | input     | wire                  | Señal de clock                                                    |
| rst                  | input     | wire                  | Señal de reset                                                    |
| encoded_tx_data      | input     | wire [DATA_WIDTH-1:0] | Datos codificados para la transmisión                             |
| encoded_tx_hdr       | input     | wire [HDR_WIDTH-1:0]  | Encabezados de los datos codificados                              |
| serdes_tx_data       | output    | wire [DATA_WIDTH-1:0] | Datos de salida para el [[Abbreviations#SERDES\|SERDES]]          |
| serdes_tx_hdr        | output    | wire [HDR_WIDTH-1:0]  | Encabezado de salida para el [[Abbreviations#SERDES\|SERDES]]     |
| cfg_tx_prbs31_enable | input     | wire                  | Señal de habilitación para la generación de secuencias [[10GBASE/PCS/PRBS31\|PRBS31]] |

## Signals

| Name                                    | Type                            | Description                                                                                       |
| --------------------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------- |
| scrambler_state_reg = {58{1'b1}}        | reg [57:0]                      | Registro para el estado del scrambler                                                             |
| scrambler_state                         | wire [57:0]                     | Estado del scrambler.                                                                             |
| scrambled_data                          | wire [DATA_WIDTH-1:0]           | Datos obtenidos luego de aplicar el scrambling.                                                   |
| prbs31_state_reg = 31'h7fffffff         | reg [30:0]                      | Registro para el estado del generador [[10GBASE/PCS/PRBS31\|PRBS31]]. Lo inicializa en 31 unos                        |
| prbs31_state                            | wire [30:0]                     | Estado del generador [[10GBASE/PCS/PRBS31\|PRBS31]].                                                                  |
| prbs31_data                             | wire [DATA_WIDTH+HDR_WIDTH-1:0] | Datos generados por el generador de [[10GBASE/PCS/PRBS31\|PRBS31]].                                                   |
| serdes_tx_data_reg = {DATA_WIDTH{1'b0}} | reg [DATA_WIDTH-1:0]            | Registro que almacena los datos que se enviarán al transmisor [[Abbreviations#SERDES\|SERDES]]    |
| serdes_tx_hdr_reg = {HDR_WIDTH{1'b0}}   | reg [HDR_WIDTH-1:0]             | Registro que almacena el encabezado que se enviará al transmisor [[Abbreviations#SERDES\|SERDES]] |
| serdes_tx_data_int                      | wire [DATA_WIDTH-1:0]           | Datos del transmisor [[Abbreviations#SERDES\|SERDES]]                                             |
| serdes_tx_hdr_int                       | wire [HDR_WIDTH-1:0]            | Encabezado del transmisor [[Abbreviations#SERDES\|SERDES]]                                        |

## Processes
- unnamed: ( @(posedge clk) )
  - **Type:** always
  - **Description**
  Actualiza los registros en cada flanco positivo del clock
 

## Instantiations

- scrambler_inst: [[10GBASE/PCS/lfsr\|lfsr]]
  -  Instancia un módulo LFSR (Linear Feedback Shift Register) para el scrambler
- prbs31_gen_inst: [[10GBASE/PCS/lfsr\|lfsr]]
  -  Instancia un módulo LFSR (Linear Feedback Shift Register) para la generación de PRBS31
