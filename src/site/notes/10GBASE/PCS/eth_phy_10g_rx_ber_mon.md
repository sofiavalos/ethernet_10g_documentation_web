---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx-ber-mon/"}
---

 **File**: [[10GBASE/PCS/eth_phy_10g_rx_ber_mon_code\|eth_phy_10g_rx_ber_mon_code]]

## Diagram
![Diagram](eth_phy_10g_rx_ber_mon.svg "Diagram")
## Description

Modulo que controla el bit error rate y activa dicha señal cuando hay más de 15 sync headers validos en 125us.

## Generics

| Generic name | Type | Value     | Description        |
| ------------ | ---- | --------- | ------------------ |
| HDR_WIDTH    |      | 2         | Ancho del header   |
| COUNT_125US  |      | 125000/10 | Contador de 125 us |

## Ports

| Port name     | Direction | Type                 | Description                     |
| ------------- | --------- | -------------------- | ------------------------------- |
| clk           | input     | wire                 | Señal de clock                  |
| rst           | input     | wire                 | Señal de reset                  |
| serdes_rx_hdr | input     | wire [HDR_WIDTH-1:0] | Serdes sync header del receptor |
| rx_high_ber   | output    | wire                 | Tasa de error de bit            |

## Signals

| Name                         | Type                  | Description                                                   |
| ---------------------------- | --------------------- | ------------------------------------------------------------- |
| time_count_reg = COUNT_125US | reg [COUNT_WIDTH-1:0] | Registro de contador de tiempo, se inicializa en COUNT_125US. |
| time_count_next              | reg [COUNT_WIDTH-1:0] | Registro de contador de tiempo, se inicializa en COUNT_125US. |
| ber_count_reg = 4'd0         | reg [3:0]             | Registro de contador de errores de header. Máximo 4 bits      |
| ber_count_next               | reg [3:0]             | Registro de contador de errores de header. Máximo 4 bits      |
| rx_high_ber_reg = 1'b0       | reg                   | Registro que indica un [[Abbreviations#BER\|BER]] alto.       |
| rx_high_ber_next             | reg                   | Registro que indica un [[Abbreviations#BER\|BER]] alto.       |

## Constants

| Name        | Type | Value | Description                                                           |
| ----------- | ---- | ----- | --------------------------------------------------------------------- |
| COUNT_WIDTH |      | $     | Determina la cantidad de bits necesarios para representar COUNT_125US |
| SYNC_DATA   |      | 2'b10 | Sync headers de sincronizacion de bloques de datos y control          |
| SYNC_CTRL   |      | 2'b01 | Sync headers de sincronizacion de bloques de datos y control          |

## Processes
- unnamed: ( @* )
  - **Type:** always
  - **Description**
Verifica si hay mas de 15 sync headers validos en un intervalo de 125us
 
- unnamed: ( @(posedge clk) )
  - **Type:** always
  - **Description**
 En cada flanco positivo de clock se actualizan los valores de los registros y se verifica la señal de reinicio 
