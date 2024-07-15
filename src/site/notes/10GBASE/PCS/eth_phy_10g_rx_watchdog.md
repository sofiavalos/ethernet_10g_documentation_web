---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx-watchdog/"}
---

- **File**: [[10GBASE/PCS/eth_phy_10g_rx_watchdog_code\|eth_phy_10g_rx_watchdog_code]]

## Diagram
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:svgjs="http://svgjs.com/svgjs" viewBox="0 0 785 210"><svg id="SvgjsSvg1002" width="2" height="0" focusable="false" style="overflow:hidden;top:-100%;left:-100%;position:absolute;opacity:0"><polyline id="SvgjsPolyline1003" points="245,0 260,0"></polyline><path id="SvgjsPath1004" d="M0 0 "></path></svg><rect id="SvgjsRect1006" width="440" height="50" fill="black" x="260" y="0"></rect><rect id="SvgjsRect1007" width="436" height="45" fill="#bdecb6" x="262" y="2"></rect><text id="SvgjsText1008" font-family="Helvetica" x="240" y="-5.698437500000001" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1009" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1010" font-family="Helvetica" x="275" y="-5.698437500000001" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1011" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   HDR_WIDTH </tspan></text><line id="SvgjsLine1012" x1="245" y1="15" x2="260" y2="15" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1013" font-family="Helvetica" x="240" y="14.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1014" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1015" font-family="Helvetica" x="275" y="14.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1016" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   COUNT_125US </tspan></text><line id="SvgjsLine1017" x1="245" y1="35" x2="260" y2="35" stroke-linecap="rec" stroke="black" stroke-width="5"></line><rect id="SvgjsRect1018" width="440" height="150" fill="black" x="260" y="55"></rect><rect id="SvgjsRect1019" width="436" height="145" fill="#fdfd96" x="262" y="57"></rect><text id="SvgjsText1020" font-family="Helvetica" x="240" y="49.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1021" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1022" font-family="Helvetica" x="275" y="49.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1023" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   clk </tspan></text><line id="SvgjsLine1024" x1="245" y1="70" x2="260" y2="70" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1025" font-family="Helvetica" x="240" y="69.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1026" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1027" font-family="Helvetica" x="275" y="69.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1028" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   rst </tspan></text><line id="SvgjsLine1029" x1="245" y1="90" x2="260" y2="90" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1030" font-family="Helvetica" x="240" y="89.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1031" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire [HDR_WIDTH-1:0] </tspan></text><text id="SvgjsText1032" font-family="Helvetica" x="275" y="89.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1033" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   serdes_rx_hdr </tspan></text><line id="SvgjsLine1034" x1="245" y1="110" x2="260" y2="110" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1035" font-family="Helvetica" x="240" y="109.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1036" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1037" font-family="Helvetica" x="275" y="109.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1038" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   rx_bad_block </tspan></text><line id="SvgjsLine1039" x1="245" y1="130" x2="260" y2="130" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1040" font-family="Helvetica" x="240" y="129.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1041" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1042" font-family="Helvetica" x="275" y="129.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1043" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   rx_sequence_error </tspan></text><line id="SvgjsLine1044" x1="245" y1="150" x2="260" y2="150" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1045" font-family="Helvetica" x="240" y="149.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1046" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1047" font-family="Helvetica" x="275" y="149.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1048" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   rx_block_lock </tspan></text><line id="SvgjsLine1049" x1="245" y1="170" x2="260" y2="170" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1050" font-family="Helvetica" x="240" y="169.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1051" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1052" font-family="Helvetica" x="275" y="169.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1053" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   rx_high_ber </tspan></text><line id="SvgjsLine1054" x1="245" y1="190" x2="260" y2="190" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1055" font-family="Helvetica" x="720" y="49.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1056" dy="26" x="720" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1057" font-family="Helvetica" x="685" y="49.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1058" dy="26" x="685" svgjs:data="{&quot;newLined&quot;:true}">   serdes_rx_reset_req </tspan></text><line id="SvgjsLine1059" x1="700" y1="70" x2="715" y2="70" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1060" font-family="Helvetica" x="720" y="69.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1061" dy="26" x="720" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1062" font-family="Helvetica" x="685" y="69.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1063" dy="26" x="685" svgjs:data="{&quot;newLined&quot;:true}">   rx_status </tspan></text><line id="SvgjsLine1064" x1="700" y1="90" x2="715" y2="90" stroke-linecap="rec" stroke="black" stroke-width="5"></line></svg>
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
