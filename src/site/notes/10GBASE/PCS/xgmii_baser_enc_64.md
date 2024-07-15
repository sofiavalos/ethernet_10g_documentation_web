---
{"dg-publish":true,"permalink":"/10-gbase/pcs/xgmii-baser-enc-64/"}
---

- **File**: [[10GBASE/MAC/xgmii_baser_enc_64_code\|xgmii_baser_enc_64_code]]

## Diagram
![Diagram](xgmii_baser_enc_64.svg "Diagram")
## Description

Módulo que decodifica la interfaz [[Abbreviations#SERDES\|SERDES]] a [[Abbreviations#XGMII\|Abbreviations#XGMII]].

## Generics

| Generic name | Type | Value          | Description      |
| ------------ | ---- | -------------- | ---------------- |
| DATA_WIDTH   |      | 64             | Ancho de datos   |
| CTRL_WIDTH   |      | (DATA_WIDTH/8) | Ancho de control |
| HDR_WIDTH    |      | 2              | Ancho de header  |

## Ports

| Port name       | Direction | Type                  | Description                                                |
| --------------- | --------- | --------------------- | ---------------------------------------------------------- |
| clk             | input     | wire                  | Señal de clock                                             |
| rst             | input     | wire                  | Señal de reset                                             |
| xgmii_txd       | input     | wire [DATA_WIDTH-1:0] | Datos de entrada [[Abbreviations#XGMII\|XGMII]]            |
| xgmii_txc       | input     | wire [CTRL_WIDTH-1:0] | Señales de control [[Abbreviations#XGMII\|XGMII]]          |
| encoded_tx_data | output    | wire [DATA_WIDTH-1:0] | Datos codificados                                          |
| encoded_tx_hdr  | output    | wire [HDR_WIDTH-1:0]  | Encabezado codificado                                      |
| tx_bad_block    | output    | wire                  | Flag que indica si hay un bloque de transmision defectuoso |

## Signals

| Name                                     | Type                     | Description                                                       |
| ---------------------------------------- | ------------------------ | ----------------------------------------------------------------- |
| encoded_ctrl                             | reg [DATA_WIDTH*7/8-1:0] | Registro para almacenar control codificado                        |
| encode_err                               | reg [CTRL_WIDTH-1:0]     | Registro para almacenar errores en codificacion                   |
| encoded_tx_data_reg = {DATA_WIDTH{1'b0}} | reg [DATA_WIDTH-1:0]     | Registro para almacenar los datos de salida codificado.           |
| encoded_tx_data_next                     | reg [DATA_WIDTH-1:0]     | Registro para almacenar los datos de salida codificado.           |
| encoded_tx_hdr_reg = {HDR_WIDTH{1'b0}}   | reg [HDR_WIDTH-1:0]      | Registro para almacenar el header de salida codificado.           |
| encoded_tx_hdr_next                      | reg [HDR_WIDTH-1:0]      | Registro para almacenar el header de salida codificado.           |
| tx_bad_block_reg = 1'b0                  | reg                      | Registro para indicar si hay un bloque de transmisión defectuoso. |
| tx_bad_block_next                        | reg                      | Registro para indicar si hay un bloque de transmisión defectuoso. |
| i                                        | integer                  |                                                                   |

## Constants

| Name                | Type | Value | Description                                                                               |
| ------------------- | ---- | ----- | ----------------------------------------------------------------------------------------- |
| XGMII_IDLE          |      | 8'h07 | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control idle                 |
| XGMII_LPI           |      | 8'h06 | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control LPI                  |
| XGMII_START         |      | 8'hfb | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control start                |
| XGMII_TERM          |      | 8'hfd | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control terminate            |
| XGMII_ERROR         |      | 8'hfe | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control error                |
| XGMII_SEQ_OS        |      | 8'h9c | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control sequence ordered set |
| XGMII_RES_0         |      | 8'h1c | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control reserved0            |
| XGMII_RES_1         |      | 8'h3c | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control reserved1            |
| XGMII_RES_2         |      | 8'h7c | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control reserved2            |
| XGMII_RES_3         |      | 8'hbc | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control reserved3            |
| XGMII_RES_4         |      | 8'hdc | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control reserved4            |
| XGMII_RES_5         |      | 8'hf7 | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control reserved5            |
| XGMII_SIG_OS        |      | 8'h5c | [[Abbreviations#XGMII\|XGMII]] Control Code para caracter de control Signal ordered set   |
| CTRL_IDLE           |      | 7'h00 | 10GBASE-R Control Code para caracter de control idle                                      |
| CTRL_LPI            |      | 7'h06 | 10GBASE-R Control Code para caracter de control LPI                                       |
| CTRL_ERROR          |      | 7'h1e | 10GBASE-R Control Code para caracter de control error                                     |
| CTRL_RES_0          |      | 7'h2d | 10GBASE-R Control Code para caracter de control reserved0                                 |
| CTRL_RES_1          |      | 7'h33 | 10GBASE-R Control Code para caracter de control reserved1                                 |
| CTRL_RES_2          |      | 7'h4b | 10GBASE-R Control Code para caracter de control reserved2                                 |
| CTRL_RES_3          |      | 7'h55 | 10GBASE-R Control Code para caracter de control reserved3                                 |
| CTRL_RES_4          |      | 7'h66 | 10GBASE-R Control Code para caracter de control reserved4                                 |
| CTRL_RES_5          |      | 7'h78 | 10GBASE-R Control Code para caracter de control reserved5                                 |
| O_SEQ_OS            |      | 4'h0  | 10GBASE-R O Code para caracter de control Sequence ordered set                            |
| O_SIG_OS            |      | 4'hf  | 10GBASE-R O Code para caracter de control Signal ordered set                              |
| SYNC_DATA           |      | 2'b10 | Header de Sincronizacion para bloque de datos                                             |
| SYNC_CTRL           |      | 2'b01 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_CTRL     |      | 8'h1e | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_OS_4     |      | 8'h2d | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_START_4  |      | 8'h33 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_OS_START |      | 8'h66 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_OS_04    |      | 8'h55 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_START_0  |      | 8'h78 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_OS_0     |      | 8'h4b | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_0   |      | 8'h87 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_1   |      | 8'h99 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_2   |      | 8'haa | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_3   |      | 8'hb4 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_4   |      | 8'hcc | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_5   |      | 8'hd2 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_6   |      | 8'he1 | Header de Sincronizacion para bloque de control                                           |
| BLOCK_TYPE_TERM_7   |      | 8'hff | Header de Sincronizacion para bloque de control                                           |

## Processes
- unnamed: ( @* )
  - **Type:** always
  - **Description**
  Codifica los datos según el caso correspondientes y los respectos codigos para cada caso
 
- unnamed: ( @(posedge clk) )
  - **Type:** always
  - **Description**
 En cada flanco positivo del clock se actualizan los registros con sus respectivos valores calculados en el bloque anterior 
