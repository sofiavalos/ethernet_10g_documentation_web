---
{"dg-publish":true,"permalink":"/10-gbase/pcs/eth-phy-10g-rx-frame-sync/"}
---

- **File**: [[10GBASE/PCS/eth_phy_10g_rx_frame_sync_code\|eth_phy_10g_rx_frame_sync_code]]

## Diagram
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:svgjs="http://svgjs.com/svgjs" viewBox="0 0 725 150"><svg id="SvgjsSvg1002" width="2" height="0" focusable="false" style="overflow:hidden;top:-100%;left:-100%;position:absolute;opacity:0"><polyline id="SvgjsPolyline1003" points="245,0 260,0"></polyline><path id="SvgjsPath1004" d="M0 0 "></path></svg><rect id="SvgjsRect1006" width="380" height="70" fill="black" x="260" y="0"></rect><rect id="SvgjsRect1007" width="376" height="65" fill="#bdecb6" x="262" y="2"></rect><text id="SvgjsText1008" font-family="Helvetica" x="240" y="-5.698437500000001" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1009" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1010" font-family="Helvetica" x="275" y="-5.698437500000001" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1011" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   HDR_WIDTH </tspan></text><line id="SvgjsLine1012" x1="245" y1="15" x2="260" y2="15" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1013" font-family="Helvetica" x="240" y="14.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1014" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1015" font-family="Helvetica" x="275" y="14.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1016" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   BITSLIP_HIGH_CYCLES </tspan></text><line id="SvgjsLine1017" x1="245" y1="35" x2="260" y2="35" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1018" font-family="Helvetica" x="240" y="34.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1019" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1020" font-family="Helvetica" x="275" y="34.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1021" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   BITSLIP_LOW_CYCLES </tspan></text><line id="SvgjsLine1022" x1="245" y1="55" x2="260" y2="55" stroke-linecap="rec" stroke="black" stroke-width="5"></line><rect id="SvgjsRect1023" width="380" height="70" fill="black" x="260" y="75"></rect><rect id="SvgjsRect1024" width="376" height="65" fill="#fdfd96" x="262" y="77"></rect><text id="SvgjsText1025" font-family="Helvetica" x="240" y="69.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1026" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1027" font-family="Helvetica" x="275" y="69.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1028" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   clk </tspan></text><line id="SvgjsLine1029" x1="245" y1="90" x2="260" y2="90" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1030" font-family="Helvetica" x="240" y="89.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1031" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1032" font-family="Helvetica" x="275" y="89.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1033" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   rst </tspan></text><line id="SvgjsLine1034" x1="245" y1="110" x2="260" y2="110" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1035" font-family="Helvetica" x="240" y="109.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1036" dy="26" x="240" svgjs:data="{&quot;newLined&quot;:true}">   wire [HDR_WIDTH-1:0] </tspan></text><text id="SvgjsText1037" font-family="Helvetica" x="275" y="109.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1038" dy="26" x="275" svgjs:data="{&quot;newLined&quot;:true}">   serdes_rx_hdr </tspan></text><line id="SvgjsLine1039" x1="245" y1="130" x2="260" y2="130" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1040" font-family="Helvetica" x="660" y="69.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1041" dy="26" x="660" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1042" font-family="Helvetica" x="625" y="69.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1043" dy="26" x="625" svgjs:data="{&quot;newLined&quot;:true}">   serdes_rx_bitslip </tspan></text><line id="SvgjsLine1044" x1="640" y1="90" x2="655" y2="90" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1045" font-family="Helvetica" x="660" y="89.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1046" dy="26" x="660" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1047" font-family="Helvetica" x="625" y="89.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1048" dy="26" x="625" svgjs:data="{&quot;newLined&quot;:true}">   rx_block_lock </tspan></text><line id="SvgjsLine1049" x1="640" y1="110" x2="655" y2="110" stroke-linecap="rec" stroke="black" stroke-width="5"></line></svg>
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
