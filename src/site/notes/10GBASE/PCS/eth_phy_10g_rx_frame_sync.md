---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx-frame-sync/"}
---

- **File**: [[10GBASE/PCS/eth_phy_10g_rx_frame_sync_code\|eth_phy_10g_rx_frame_sync_code]]

## Diagram
![Diagram](eth_phy_10g_rx_frame_sync.svg "Diagram")
## Description

Modulo que verifica la sincronización del header y activa block_lock en caso que corresponda.

## Generics

| Generic name        | Type | Value | Description                                                                                |
| ------------------- | ---- | ----- | ------------------------------------------------------------------------------------------ |
| HDR_WIDTH           |      | 2     | Ancho de encabezado                                                                        |
| BITSLIP_HIGH_CYCLES |      | 1     | 1 ciclo de reloj para realizar un desplazamiento cuando se detecta una desalineacion alta  |
| BITSLIP_LOW_CYCLES  |      | 8     | 8 ciclos de reloj para realizar un desplazamiento cuando se detecta una desalineación baja |

## Ports

| Port name         | Direction | Type                 | Description                                                        |
| ----------------- | --------- | -------------------- | ------------------------------------------------------------------ |
| clk               | input     | wire                 | Señal de clock                                                     |
| rst               | input     | wire                 | Señal de reinicio                                                  |
| serdes_rx_hdr     | input     | wire [HDR_WIDTH-1:0] | Señal de [[Abbreviations#SERDES\|SERDES]] sync header              |
| serdes_rx_bitslip | output    | wire                 | Señal de [[Abbreviations#SERDES\|SERDES]] bitslip                  |
| rx_block_lock     | output    | wire                 | Señal de salida que indica si se detectaron 64 sync header validos |

## Signals

| Name                         | Type                          | Description                                                                                  |
| ---------------------------- | ----------------------------- | -------------------------------------------------------------------------------------------- |
| sh_count_reg = 6'd0          | reg [5:0]                     | Registro que almacena la cuenta de sync headers totales recibidos. Máximo 64                 |
| sh_count_next                | reg [5:0]                     | Registro que almacena la cuenta de sync headers totales recibidos. Máximo 64                 |
| sh_invalid_count_reg = 4'd0  | reg [3:0]                     | Registro que almacena la cuenta de sync headers inválidos recibidos. Máximo 16               |
| sh_invalid_count_next        | reg [3:0]                     | Registro que almacena la cuenta de sync headers inválidos recibidos. Máximo 16               |
| bitslip_count_reg = 0        | reg [BITSLIP_COUNT_WIDTH-1:0] | Registro que almacena la cuenta para controlar el bitslip en la recepción de datos. Máximo 8 |
| bitslip_count_next           | reg [BITSLIP_COUNT_WIDTH-1:0] | Registro que almacena la cuenta para controlar el bitslip en la recepción de datos. Máximo 8 |
| serdes_rx_bitslip_reg = 1'b0 | reg                           | Registro para la señal de serdes bitslip                                                     |
| serdes_rx_bitslip_next       | reg                           | Registro para la señal de serdes bitslip                                                     |
| rx_block_lock_reg = 1'b0     | reg                           | Registro para el bloque de alineacion                                                        |
| rx_block_lock_next           | reg                           | Registro para el bloque de alineacion                                                        |

## Constants

| Name                | Type | Value                                                                               | Description                                                                                      |
| ------------------- | ---- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| BITSLIP_MAX_CYCLES  |      | BITSLIP_HIGH_CYCLES > BITSLIP_LOW_CYCLES ? BITSLIP_HIGH_CYCLES : BITSLIP_LOW_CYCLES | Determina el límite máximo de ciclos para el bitslip                                             |
| BITSLIP_COUNT_WIDTH |      | $                                                                                   | Determina la cantidad de bits necesarios para representar el número de ciclos máximos de bitslip |
| SYNC_DATA           |      | 2'b10                                                                               |                                                                                                  |
| SYNC_CTRL           |      | 2'b01                                                                               |                                                                                                  |

## Processes
- unnamed: ( @* )
  - **Type:** always
  - **Description**
Verifica si se alineo correctamente el bloque, esto es con 64 headers validos y 0 invalidos. Una vez conseguida, la flag de alineacion se mantiene siempre y cuando haya menos de 15 encabezados invalidos en porciones de 64 en 64 headers. En caso de que llegue un encabezado invalido antes de tener la flag activa, se activa el bitslip y espera 8 encabezados validos antes de volver a contar los encabezados.
 
- unnamed: ( @(posedge clk) )
  - **Type:** always
  - **Description**
 En cada flanco positivo de clock se actualizan los registros y se verifica el estado de la señal de reinicio .
