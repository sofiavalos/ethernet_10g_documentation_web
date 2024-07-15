---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx-if/"}
---

- **File**: [[10GBASE/PCS/eth_phy_10g_rx_if_code\|eth_phy_10g_rx_if_code]]

## Diagram
![Diagram](eth_phy_10g_rx_if.svg "Diagram")

## Hierarchical structure
![rx_if_compuesto.png](/img/user/10GBASE/PCS/rx_if_compuesto.png)
## Description

Modulo que controla los bloques del receptor con interfaz SERDES. Puede o no generar PRSB31, Además de controlar la sincronización del header activando la flag de block lock si hay  64 headers consecutivos sin errores, dicha flag permanece activa siempre y cuando no haya más de 16 headers inválidos en intervalos de 64 headers.
También controla si hay una tasa de [[Abbreviations#BER\|BER]] alta y monitorea el receptor para ver si es necesario solicitar un reset o activar pcs_status en caso de que se este en block_lock y no haya un [[Abbreviations#BER\|BER]] alto en 125us.

## Generics

| Generic name        | Type | Value     | Description                                  |
| ------------------- | ---- | --------- | -------------------------------------------- |
| DATA_WIDTH          |      | 64        | Ancho de bus de datos                        |
| HDR_WIDTH           |      | 2         | Ancho de bus de header                       |
| BIT_REVERSE         |      | 0         | Flag para habilitar reversión de bits        |
| SCRAMBLER_DISABLE   |      | 0         | Flag para habilitar scrambler                |
| PRBS31_ENABLE       |      | 0         | Flag para habilitar [[10GBASE/PCS/PRBS31\|PRBS31]]               |
| SERDES_PIPELINE     |      | 0         | Flag para habilitar profundidad del pipeline |
| BITSLIP_HIGH_CYCLES |      | 1         | Ciclos de bitslip alto                       |
| BITSLIP_LOW_CYCLES  |      | 8         | Ciclos de bitslip bajo                       |
| COUNT_125US         |      | 125000/10 | Contador de 125 us                           |

## Ports

| Port name            | Direction | Type                  | Description                                 |
| -------------------- | --------- | --------------------- | ------------------------------------------- |
| clk                  | input     | wire                  | Señal del clock                             |
| rst                  | input     | wire                  | Señal de reset                              |
| encoded_rx_data      | output    | wire [DATA_WIDTH-1:0] | Datos codificados                           |
| encoded_rx_hdr       | output    | wire [HDR_WIDTH-1:0]  | Header codificado                           |
| serdes_rx_data       | input     | wire [DATA_WIDTH-1:0] | Entrada de bloques de datos interfaz serdes |
| serdes_rx_hdr        | input     | wire [HDR_WIDTH-1:0]  | Entrada del sync header interfaz serdes     |
| serdes_rx_bitslip    | output    | wire                  | Salida del bitslip                          |
| serdes_rx_reset_req  | output    | wire                  | Salida de solicitud de reinicio             |
| rx_bad_block         | input     | wire                  | Flag de bloque con error                    |
| rx_sequence_error    | input     | wire                  | Flag de error de secuencia                  |
| rx_error_count       | output    | wire [6:0]            | Contador de errores                         |
| rx_block_lock        | output    | wire                  | Flag de bloque alineado                     |
| rx_high_ber          | output    | wire                  | Flag de bit rate error alto                 |
| rx_status            | output    | wire                  | Flag del estado del receptor                |
| cfg_rx_prbs31_enable | input     | wire                  | Entrada para habilitar la [[10GBASE/PCS/PRBS31\|PRBS31]]        |

## Signals

| Name                                     | Type                            | Description                                                              |
| ---------------------------------------- | ------------------------------- | ------------------------------------------------------------------------ |
| serdes_rx_data_rev                       | wire [DATA_WIDTH-1:0]           | Señales para procesar los datos del [[Abbreviations#SERDES\|SERDES]]     |
| serdes_rx_data_int                       | wire [DATA_WIDTH-1:0]           | Señales para procesar los datos del [[Abbreviations#SERDES\|SERDES]]     |
| serdes_rx_hdr_rev                        | wire [HDR_WIDTH-1:0]            | Señales para procesar el encabezado del [[Abbreviations#SERDES\|SERDES]] |
| serdes_rx_hdr_int                        | wire [HDR_WIDTH-1:0]            | Señales para procesar el encabezado del [[Abbreviations#SERDES\|SERDES]] |
| descrambled_rx_data                      | wire [DATA_WIDTH-1:0]           | Almacena los datos descifrados despues del proceso de descambler         |
| encoded_rx_data_reg = {DATA_WIDTH{1'b0}} | reg [DATA_WIDTH-1:0]            | Registro para almacenar los datos codificados                            |
| encoded_rx_hdr_reg = {HDR_WIDTH{1'b0}}   | reg [HDR_WIDTH-1:0]             | Registro para almacenar el encabezado codificado                         |
| scrambler_state_reg = {58{1'b1}}         | reg [57:0]                      | Registro de estado del scrambler                                         |
| scrambler_state                          | wire [57:0]                     |                                                                          |
| prbs31_state_reg = 31'h7fffffff          | reg [30:0]                      | Estado del generador de [[10GBASE/PCS/PRBS31\|PRBS31]]                                       |
| prbs31_state                             | wire [30:0]                     |                                                                          |
| prbs31_data                              | wire [DATA_WIDTH+HDR_WIDTH-1:0] | Almacena los datos de salida del generador [[10GBASE/PCS/PRBS31\|PRBS31]]                    |
| prbs31_data_reg = 0                      | reg [DATA_WIDTH+HDR_WIDTH-1:0]  |                                                                          |
| rx_error_count_reg = 0                   | reg [6:0]                       | Contadores de errores                                                    |
| rx_error_count_1_reg = 0                 | reg [5:0]                       |                                                                          |
| rx_error_count_2_reg = 0                 | reg [5:0]                       |                                                                          |
| rx_error_count_1_temp = 0                | reg [5:0]                       |                                                                          |
| rx_error_count_2_temp = 0                | reg [5:0]                       |                                                                          |
| i                                        | integer                         |                                                                          |
| serdes_rx_bitslip_int                    | wire                            | Señal que activa el bitslip                                              |
| serdes_rx_reset_req_int                  | wire                            | Señal que solicita reset                                                 |

## Processes
- unnamed: ( @* )
  - **Type:** always
  - **Description**
 Calcula el conteo de errores a partir de los datos del generador [[10GBASE/PCS/PRBS31\|PRBS31]], actualiza los registros de error_count 
- unnamed: ( @(posedge clk) )
  - **Type:** always
  - **Description**
 En cada flanco positivo del clock se actualizan los registros y si [[10GBASE/PCS/PRBS31\|PRBS31]] está activado calcula el conteo de errores acumulativo 

## Instantiations

- descrambler_inst: [[10GBASE/PCS/lfsr\|lfsr]]
  -  Instancia un módulo LFSR (Linear Feedback Shift Register) llamado para el scrambler
- prbs31_check_inst: [[10GBASE/PCS/lfsr\|lfsr]]
  -  Instancia un módulo LFSR (Linear Feedback Shift Register) para la generación de [[10GBASE/PCS/PRBS31\|PRBS31]]
- eth_phy_10g_rx_frame_sync_inst: [[10GBASE/PCS/eth_phy_10g_rx_frame_sync\|eth_phy_10g_rx_frame_sync]]
  -  Instancia un módulo de sincronizacion del frame
- eth_phy_10g_rx_ber_mon_inst: [[10GBASE/PCS/eth_phy_10g_rx_ber_mon\|eth_phy_10g_rx_ber_mon]]
  -  Instancia un módulo para monitorear el [[Abbreviations#BER\|BER]]
- eth_phy_10g_rx_watchdog_inst: [[10GBASE/PCS/eth_phy_10g_rx_watchdog\|eth_phy_10g_rx_watchdog]]
  -  Instancia un modulo para monitoreo de los errores y estado del receptor
