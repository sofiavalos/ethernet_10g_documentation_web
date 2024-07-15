---
{"dg-publish":true,"permalink":"/10-gbase/mac/mac-pause-ctrl-rx/"}
---

# Entity: mac_pause_ctrl_rx 
- **File**: [[mac_pause_ctrl_rx.v]]

## Diagram
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:svgjs="http://svgjs.com/svgjs" viewBox="0 0 915 430"><svg id="SvgjsSvg1002" width="2" height="0" focusable="false" style="overflow:hidden;top:-100%;left:-100%;position:absolute;opacity:0"><polyline id="SvgjsPolyline1003" points="325,0 340,0"></polyline><path id="SvgjsPath1004" d="M0 0 "></path></svg><rect id="SvgjsRect1006" width="430" height="50" fill="black" x="340" y="0"></rect><rect id="SvgjsRect1007" width="426" height="45" fill="#bdecb6" x="342" y="2"></rect><text id="SvgjsText1008" font-family="Helvetica" x="320" y="-5.698437500000001" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1009" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1010" font-family="Helvetica" x="355" y="-5.698437500000001" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1011" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   MCF_PARAMS_SIZE </tspan></text><line id="SvgjsLine1012" x1="325" y1="15" x2="340" y2="15" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1013" font-family="Helvetica" x="320" y="14.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1014" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">    </tspan></text><text id="SvgjsText1015" font-family="Helvetica" x="355" y="14.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1016" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   PFC_ENABLE </tspan></text><line id="SvgjsLine1017" x1="325" y1="35" x2="340" y2="35" stroke-linecap="rec" stroke="black" stroke-width="5"></line><rect id="SvgjsRect1018" width="430" height="370" fill="black" x="340" y="55"></rect><rect id="SvgjsRect1019" width="426" height="365" fill="#fdfd96" x="342" y="57"></rect><text id="SvgjsText1020" font-family="Helvetica" x="320" y="49.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1021" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1022" font-family="Helvetica" x="355" y="49.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1023" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   clk </tspan></text><line id="SvgjsLine1024" x1="325" y1="70" x2="340" y2="70" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1025" font-family="Helvetica" x="320" y="69.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1026" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1027" font-family="Helvetica" x="355" y="69.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1028" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   rst </tspan></text><line id="SvgjsLine1029" x1="325" y1="90" x2="340" y2="90" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1030" font-family="Helvetica" x="320" y="89.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1031" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1032" font-family="Helvetica" x="355" y="89.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1033" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   mcf_valid </tspan></text><line id="SvgjsLine1034" x1="325" y1="110" x2="340" y2="110" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1035" font-family="Helvetica" x="320" y="109.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1036" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [47:0] </tspan></text><text id="SvgjsText1037" font-family="Helvetica" x="355" y="109.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1038" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   mcf_eth_dst </tspan></text><line id="SvgjsLine1039" x1="325" y1="130" x2="340" y2="130" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1040" font-family="Helvetica" x="320" y="129.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1041" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [47:0] </tspan></text><text id="SvgjsText1042" font-family="Helvetica" x="355" y="129.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1043" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   mcf_eth_src </tspan></text><line id="SvgjsLine1044" x1="325" y1="150" x2="340" y2="150" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1045" font-family="Helvetica" x="320" y="149.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1046" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [15:0] </tspan></text><text id="SvgjsText1047" font-family="Helvetica" x="355" y="149.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1048" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   mcf_eth_type </tspan></text><line id="SvgjsLine1049" x1="325" y1="170" x2="340" y2="170" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1050" font-family="Helvetica" x="320" y="169.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1051" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [15:0] </tspan></text><text id="SvgjsText1052" font-family="Helvetica" x="355" y="169.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1053" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   mcf_opcode </tspan></text><line id="SvgjsLine1054" x1="325" y1="190" x2="340" y2="190" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1055" font-family="Helvetica" x="320" y="189.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1056" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [MCF_PARAMS_SIZE\*8-1:0] </tspan></text><text id="SvgjsText1057" font-family="Helvetica" x="355" y="189.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1058" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   mcf_params </tspan></text><line id="SvgjsLine1059" x1="325" y1="210" x2="340" y2="210" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1060" font-family="Helvetica" x="320" y="209.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1061" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1062" font-family="Helvetica" x="355" y="209.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1063" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   rx_lfc_en </tspan></text><line id="SvgjsLine1064" x1="325" y1="230" x2="340" y2="230" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1065" font-family="Helvetica" x="320" y="229.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1066" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1067" font-family="Helvetica" x="355" y="229.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1068" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   rx_lfc_ack </tspan></text><line id="SvgjsLine1069" x1="325" y1="250" x2="340" y2="250" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1070" font-family="Helvetica" x="320" y="249.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1071" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [7:0] </tspan></text><text id="SvgjsText1072" font-family="Helvetica" x="355" y="249.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1073" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   rx_pfc_en </tspan></text><line id="SvgjsLine1074" x1="325" y1="270" x2="340" y2="270" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1075" font-family="Helvetica" x="320" y="269.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1076" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [7:0] </tspan></text><text id="SvgjsText1077" font-family="Helvetica" x="355" y="269.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1078" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   rx_pfc_ack </tspan></text><line id="SvgjsLine1079" x1="325" y1="290" x2="340" y2="290" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1080" font-family="Helvetica" x="320" y="289.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1081" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [15:0] </tspan></text><text id="SvgjsText1082" font-family="Helvetica" x="355" y="289.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1083" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   cfg_rx_lfc_opcode </tspan></text><line id="SvgjsLine1084" x1="325" y1="310" x2="340" y2="310" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1085" font-family="Helvetica" x="320" y="309.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1086" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1087" font-family="Helvetica" x="355" y="309.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1088" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   cfg_rx_lfc_en </tspan></text><line id="SvgjsLine1089" x1="325" y1="330" x2="340" y2="330" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1090" font-family="Helvetica" x="320" y="329.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1091" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [15:0] </tspan></text><text id="SvgjsText1092" font-family="Helvetica" x="355" y="329.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1093" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   cfg_rx_pfc_opcode </tspan></text><line id="SvgjsLine1094" x1="325" y1="350" x2="340" y2="350" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1095" font-family="Helvetica" x="320" y="349.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1096" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1097" font-family="Helvetica" x="355" y="349.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1098" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   cfg_rx_pfc_en </tspan></text><line id="SvgjsLine1099" x1="325" y1="370" x2="340" y2="370" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1100" font-family="Helvetica" x="320" y="369.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1101" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire [9:0] </tspan></text><text id="SvgjsText1102" font-family="Helvetica" x="355" y="369.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1103" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   cfg_quanta_step </tspan></text><line id="SvgjsLine1104" x1="325" y1="390" x2="340" y2="390" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1105" font-family="Helvetica" x="320" y="389.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1106" dy="26" x="320" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1107" font-family="Helvetica" x="355" y="389.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1108" dy="26" x="355" svgjs:data="{&quot;newLined&quot;:true}">   cfg_quanta_clk_en </tspan></text><line id="SvgjsLine1109" x1="325" y1="410" x2="340" y2="410" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1110" font-family="Helvetica" x="790" y="49.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1111" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1112" font-family="Helvetica" x="755" y="49.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1113" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   rx_lfc_req </tspan></text><line id="SvgjsLine1114" x1="770" y1="70" x2="785" y2="70" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1115" font-family="Helvetica" x="790" y="69.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1116" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire [7:0] </tspan></text><text id="SvgjsText1117" font-family="Helvetica" x="755" y="69.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1118" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   rx_pfc_req </tspan></text><line id="SvgjsLine1119" x1="770" y1="90" x2="785" y2="90" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1120" font-family="Helvetica" x="790" y="89.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1121" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1122" font-family="Helvetica" x="755" y="89.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1123" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_lfc_pkt </tspan></text><line id="SvgjsLine1124" x1="770" y1="110" x2="785" y2="110" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1125" font-family="Helvetica" x="790" y="109.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1126" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1127" font-family="Helvetica" x="755" y="109.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1128" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_lfc_xon </tspan></text><line id="SvgjsLine1129" x1="770" y1="130" x2="785" y2="130" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1130" font-family="Helvetica" x="790" y="129.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1131" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1132" font-family="Helvetica" x="755" y="129.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1133" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_lfc_xoff </tspan></text><line id="SvgjsLine1134" x1="770" y1="150" x2="785" y2="150" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1135" font-family="Helvetica" x="790" y="149.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1136" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1137" font-family="Helvetica" x="755" y="149.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1138" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_lfc_paused </tspan></text><line id="SvgjsLine1139" x1="770" y1="170" x2="785" y2="170" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1140" font-family="Helvetica" x="790" y="169.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1141" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire </tspan></text><text id="SvgjsText1142" font-family="Helvetica" x="755" y="169.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1143" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_pfc_pkt </tspan></text><line id="SvgjsLine1144" x1="770" y1="190" x2="785" y2="190" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1145" font-family="Helvetica" x="790" y="189.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1146" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire [7:0] </tspan></text><text id="SvgjsText1147" font-family="Helvetica" x="755" y="189.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1148" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_pfc_xon </tspan></text><line id="SvgjsLine1149" x1="770" y1="210" x2="785" y2="210" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1150" font-family="Helvetica" x="790" y="209.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1151" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire [7:0] </tspan></text><text id="SvgjsText1152" font-family="Helvetica" x="755" y="209.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1153" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_pfc_xoff </tspan></text><line id="SvgjsLine1154" x1="770" y1="230" x2="785" y2="230" stroke-linecap="rec" stroke="black" stroke-width="5"></line><text id="SvgjsText1155" font-family="Helvetica" x="790" y="229.3015625" font-size="20" text-anchor="start" family="Helvetica" size="20" anchor="start" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1156" dy="26" x="790" svgjs:data="{&quot;newLined&quot;:true}">   wire [7:0] </tspan></text><text id="SvgjsText1157" font-family="Helvetica" x="755" y="229.3015625" font-size="20" text-anchor="end" family="Helvetica" size="20" anchor="end" svgjs:data="{&quot;leading&quot;:&quot;1.3&quot;}"><tspan id="SvgjsTspan1158" dy="26" x="755" svgjs:data="{&quot;newLined&quot;:true}">   stat_rx_pfc_paused </tspan></text><line id="SvgjsLine1159" x1="770" y1="250" x2="785" y2="250" stroke-linecap="rec" stroke="black" stroke-width="5"></line></svg>
## Description

implementa la recepción y gestión de marcos de control [MAC](Abbreviations#MAC), incluyendo tanto el flujo de control a nivel de enlace (LFC), como el flujo de control de prioridad (PFC).

## Generics

| Generic name    | Type | Value | Description                                       |
| --------------- | ---- | ----- | ------------------------------------------------- |
| MCF_PARAMS_SIZE |      | 18    | Tamaño de los parámetros del marco de control MAC |
| PFC_ENABLE      |      | 1     | Habilitar PFC (Control de Flujo de Prioridad)     |

## Ports

| Port name          | Direction | Type                         | Description                                                |
| ------------------ | --------- | ---------------------------- | ---------------------------------------------------------- |
| clk                | input     | wire                         | Señal de clock                                             |
| rst                | input     | wire                         | Señal de reset                                             |
| mcf_valid          | input     | wire                         | Validez del marco de control MAC                           |
| mcf_eth_dst        | input     | wire [47:0]                  | Destino Ethernet del marco de control MAC                  |
| mcf_eth_src        | input     | wire [47:0]                  | Origen Ethernet del marco de control MAC                   |
| mcf_eth_type       | input     | wire [15:0]                  | Tipo Ethernet del marco de control MAC                     |
| mcf_opcode         | input     | wire [15:0]                  | Código de operación del marco de control MAC               |
| mcf_params         | input     | wire [MCF_PARAMS_SIZE*8-1:0] | Parámetros del marco de control MAC                        |
| rx_lfc_en          | input     | wire                         | Habilitar LFC (Control de Flujo a Nivel de Enlace)         |
| rx_lfc_req         | output    | wire                         | Solicitud de LFC (Control de Flujo a Nivel de Enlace)      |
| rx_lfc_ack         | input     | wire                         | Reconocimiento de LFC (Control de Flujo a Nivel de Enlace) |
| rx_pfc_en          | input     | wire [7:0]                   | Habilitar PFC (Control de Flujo de Prioridad)              |
| rx_pfc_req         | output    | wire [7:0]                   | Solicitud de PFC (Control de Flujo de Prioridad)           |
| rx_pfc_ack         | input     | wire [7:0]                   | Reconocimiento de PFC (Control de Flujo de Prioridad)      |
| cfg_rx_lfc_opcode  | input     | wire [15:0]                  | Código de operación de LFC configurado                     |
| cfg_rx_lfc_en      | input     | wire                         | Habilitar LFC configurado                                  |
| cfg_rx_pfc_opcode  | input     | wire [15:0]                  | Código de operación de PFC configurado                     |
| cfg_rx_pfc_en      | input     | wire                         | Habilitar PFC configurado                                  |
| cfg_quanta_step    | input     | wire [9:0]                   | Paso de cuantum configurado                                |
| cfg_quanta_clk_en  | input     | wire                         | Habilitar reloj de cuantum configurado                     |
| stat_rx_lfc_pkt    | output    | wire                         | Paquete recibido de LFC                                    |
| stat_rx_lfc_xon    | output    | wire                         | XON recibido de LFC                                        |
| stat_rx_lfc_xoff   | output    | wire                         | XOFF recibido de LFC                                       |
| stat_rx_lfc_paused | output    | wire                         | Estado pausado de LFC                                      |
| stat_rx_pfc_pkt    | output    | wire                         | Paquete recibido de PFC                                    |
| stat_rx_pfc_xon    | output    | wire [7:0]                   | XON recibido de PFC                                        |
| stat_rx_pfc_xoff   | output    | wire [7:0]                   | XOFF recibido de PFC                                       |
| stat_rx_pfc_paused | output    | wire [7:0]                   | Estado pausado de PFC                                      |

## Signals

| Name                        | Type             | Description                                                         |
| --------------------------- | ---------------- | ------------------------------------------------------------------- |
| lfc_req_reg = 1'b0          | reg              | Registro para solicitud de LFC (Control de Flujo a Nivel de Enlace) |
| lfc_req_next                | reg              | Registro para solicitud de LFC (Control de Flujo a Nivel de Enlace) |
| pfc_req_reg = 8'd0          | reg [7:0]        | Registro para solicitud de PFC (Control de Flujo de Prioridad)      |
| pfc_req_next                | reg [7:0]        | Registro para solicitud de PFC (Control de Flujo de Prioridad)      |
| lfc_quanta_reg = 0          | reg [16+QFB-1:0] | Registro para cuantum de LFC                                        |
| lfc_quanta_next             | reg [16+QFB-1:0] | Registro para cuantum de LFC                                        |
| pfc_quanta_reg[0:7]         | reg [16+QFB-1:0] | Registros para cuantum de PFC para cada cola                        |
| pfc_quanta_next[0:7]        | reg [16+QFB-1:0] | Registros para cuantum de PFC para cada cola                        |
| stat_rx_lfc_pkt_reg = 1'b0  | reg              | Registro para indicar paquete recibido de LFC                       |
| stat_rx_lfc_pkt_next        | reg              | Registro para indicar paquete recibido de LFC                       |
| stat_rx_lfc_xon_reg = 1'b0  | reg              | Registro para indicar XON recibido de LFC                           |
| stat_rx_lfc_xon_next        | reg              | Registro para indicar XON recibido de LFC                           |
| stat_rx_lfc_xoff_reg = 1'b0 | reg              | Registro para indicar XOFF recibido de LFC                          |
| stat_rx_lfc_xoff_next       | reg              | Registro para indicar XOFF recibido de LFC                          |
| stat_rx_pfc_pkt_reg = 1'b0  | reg              | Registro para indicar paquete recibido de PFC                       |
| stat_rx_pfc_pkt_next        | reg              | Registro para indicar paquete recibido de PFC                       |
| stat_rx_pfc_xon_reg = 8'd0  | reg [7:0]        | Registro para indicar XON recibido de PFC                           |
| stat_rx_pfc_xon_next        | reg [7:0]        | Registro para indicar XON recibido de PFC                           |
| stat_rx_pfc_xoff_reg = 8'd0 | reg [7:0]        | Registro para indicar XOFF recibido de PFC                          |
| stat_rx_pfc_xoff_next       | reg [7:0]        | Registro para indicar XOFF recibido de PFC                          |
| k                           | integer          |                                                                     |

## Constants

| Name | Type | Value | Description |
| ---- | ---- | ----- | ----------- |
| QFB  |      | 8     |             |

## Processes
- unnamed: ( @* )
  - **Type:** always
  - **Description**
  Gestiona el control de cuantum y las solicitudes de control de flujo tanto a nivel de enlace (LFC) como de prioridad (PFC) 
- unnamed: ( @(posedge clk) )
  - **Type:** always
  - **Description**
  Actualiza los datos en los flancos positivos de reloj 