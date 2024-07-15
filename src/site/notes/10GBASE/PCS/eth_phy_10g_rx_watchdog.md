---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx-watchdog/"}
---

- **File**: [[10GBASE/PCS/eth_phy_10g_rx_watchdog_code\|eth_phy_10g_rx_watchdog_code]]

## Diagram
![Diagram](eth_phy_10g_rx_watchdog.svg "Diagram")
## Description

Modulo que verifica el estado del header, pidiendo reset si es necesario o activando rx_status si no hay más de 16 errores en 125us.

## Generics

| Generic name | Type | Value      | Description        |
| ------------ | ---- | ---------- | ------------------ |
| HDR_WIDTH    |      | 2          | Ancho de header    |
| COUNT_125US  |      | 125000/6.4 | Contador de 125 us |

## Ports

| Port name           | Direction | Type                 | Description                                 |
| ------------------- | --------- | -------------------- | ------------------------------------------- |
| clk                 | input     | wire                 | Señal de clock                              |
| rst                 | input     | wire                 | Señal de reinicio                           |
| serdes_rx_hdr       | input     | wire [HDR_WIDTH-1:0] | Serdes sync header del rx                   |
| serdes_rx_reset_req | output    | wire                 | Solicitud de reset del serdes               |
| rx_bad_block        | input     | wire                 | Indicador de error en el bloque recibido    |
| rx_sequence_error   | input     | wire                 | Indicador de error en la secuencia recibida |
| rx_block_lock       | input     | wire                 | Indicador de si el bloque está alineado     |
| rx_high_ber         | input     | wire                 | Indicador si el ber rate error es alto      |
| rx_status           | output    | wire                 | Salida del estado del receptor              |

## Signals

| Name                           | Type                  | Description                                                   |
| ------------------------------ | --------------------- | ------------------------------------------------------------- |
| time_count_reg = 0             | reg [COUNT_WIDTH-1:0] | Registro de contador de tiempo, se inicializa en COUNT_125US. |
| time_count_next                | reg [COUNT_WIDTH-1:0] | Registro de contador de tiempo, se inicializa en COUNT_125US. |
| error_count_reg = 0            | reg [3:0]             | Registro de contador de errores. Máximo 16 bits               |
| error_count_next               | reg [3:0]             | Registro de contador de errores. Máximo 16 bits               |
| status_count_reg = 0           | reg [3:0]             | Registro de contador de estado. Máximo 16 bits                |
| status_count_next              | reg [3:0]             | Registro de contador de estado. Máximo 16 bits                |
| saw_ctrl_sh_reg = 1'b0         | reg                   | Indicador de control                                          |
| saw_ctrl_sh_next               | reg                   | Indicador de control                                          |
| block_error_count_reg = 0      | reg [9:0]             | Contador de errores de bloque                                 |
| block_error_count_next         | reg [9:0]             | Contador de errores de bloque                                 |
| serdes_rx_reset_req_reg = 1'b0 | reg                   | Indicador de solicitud de reinicio.                           |
| serdes_rx_reset_req_next       | reg                   | Indicador de solicitud de reinicio.                           |
| rx_status_reg = 1'b0           | reg                   | Indicador del estado de la recepcion.                         |
| rx_status_next                 | reg                   | Indicador del estado de la recepcion.                         |

## Constants

| Name        | Type | Value | Description                                                           |
| ----------- | ---- | ----- | --------------------------------------------------------------------- |
| COUNT_WIDTH |      | $     | Determina la cantidad de bits necesarios para representar COUNT_125US |
| SYNC_DATA   |      | 2'b10 | Encabezados de sync headers de bloques de datos y control             |
| SYNC_CTRL   |      | 2'b01 | Encabezados de sync headers de bloques de datos y control             |

## Processes
- unnamed: ( @* )
  - **Type:** always
  - **Description**
Si el sync header es de bloques de control, verifica que no haya errores, si hay menos de 16 por 125us, activa el rx_status.
Si antes de los 125us los errores son mayores a 16, activa el reset_req
 
- unnamed: ( @(posedge clk) )
  - **Type:** always
  - **Description**
 En cada flanco positivo de clock se actualizan los valores de los registros y se verifica la señal de reinicio 
- unnamed: ( @(posedge clk or posedge rst) )
  - **Type:** always
  - **Description**
 En cada flanco positivo de clock o señal de reinicio actualiza el reset req 
