---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx-ber-mon/"}
---

 **File**: [[10GBASE/PCS/eth_phy_10g_rx_ber_mon_code\|eth_phy_10g_rx_ber_mon_code]]

## Diagram
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:svgjs="http://svgjs.com/svgjs" viewBox="0 0 665 130"><svg id="SvgjsSvg1002" width="2" height="0" focusable="false" style="overflow:hidden;top:-100%;left:-100%;position:absolute;opacity:0"><polyline id="SvgjsPolyline1003" points="245,0 260,0"></polyline><path id="SvgjsPath1004" d="M0 0 "></path></svg><rect id="SvgjsRect1006" width="320" height="50" fill="black" x="260" y="0"></rect><rect id="SvgjsRect1007" width="316" height="45" fill="#bdecb6" x="262" y="2"></rect><text id="SvgjsText1008" font-family="Helvetica" x="240" y="-5.698437500000001" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1009" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1010" font-family="Helvetica" x="275" y="-5.698437500000001" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1011" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   HDR_WIDTH </tspan></text><line id="SvgjsLine1012" x1="245" y1="15" x2="260" y2="15" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1013" font-family="Helvetica" x="240" y="14.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1014" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1015" font-family="Helvetica" x="275" y="14.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1016" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   COUNT_125US </tspan></text><line id="SvgjsLine1017" x1="245" y1="35" x2="260" y2="35" stroke-linecap="rec" stroke="black" stroke-width="5"></line><rect id="SvgjsRect1018" width="320" height="70" fill="black" x="260" y="55"></rect><rect id="SvgjsRect1019" width="316" height="65" fill="#fdfd96" x="262" y="57"></rect><text id="SvgjsText1020" font-family="Helvetica" x="240" y="49.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1021" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1022" font-family="Helvetica" x="275" y="49.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1023" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   clk </tspan></text><line id="SvgjsLine1024" x1="245" y1="70" x2="260" y2="70" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1025" font-family="Helvetica" x="240" y="69.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1026" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1027" font-family="Helvetica" x="275" y="69.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1028" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   rst </tspan></text><line id="SvgjsLine1029" x1="245" y1="90" x2="260" y2="90" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1030" font-family="Helvetica" x="240" y="89.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1031" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire [HDR_WIDTH-1:0] </tspan></text><text id="SvgjsText1032" font-family="Helvetica" x="275" y="89.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1033" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   serdes_rx_hdr </tspan></text><line id="SvgjsLine1034" x1="245" y1="110" x2="260" y2="110" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1035" font-family="Helvetica" x="600" y="49.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1036" dy="26" x="600" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1037" font-family="Helvetica" x="565" y="49.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1038" dy="26" x="565" svgjs:data="{&quot;newLined&quot;:true}">   rx_high_ber </tspan></text><line id="SvgjsLine1039" x1="580" y1="70" x2="595" y2="70" stroke-linecap="rec" stroke="black" stroke-width="5"></line></svg>
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
| rx_high_ber_reg = 1'b0       | reg                   | Registro que indica un [[10GBASE/Abbreviations#BER\|BER]] alto.       |
| rx_high_ber_next             | reg                   | Registro que indica un [[10GBASE/Abbreviations#BER\|BER]] alto.       |

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
