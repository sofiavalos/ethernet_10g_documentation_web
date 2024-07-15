---
{"dg-publish":true,"permalink":"/10-gbase/pcs/lfsr/"}
---

- **File**: [[10GBASE/MAC/lfsr_code\|lfsr_code]]

## Diagram
![Diagram](lfsr.svg "Diagram")
## Generics

| Generic name      | Type | Value        | Description                                           |
| ----------------- | ---- | ------------ | ----------------------------------------------------- |
| LFSR_WIDTH        |      | 31           | Ancho del LFSR                                        |
| LFSR_POLY         |      | 31'h10000001 | Polinomio del LFSR                                    |
| LFSR_CONFIG       |      | "FIBONACCI"  | Configuracion del LFSR: "GALOIS", "FIBONACCI"         |
| LFSR_FEED_FORWARD |      | 0            | LFSR feed forward enable:                             |
| REVERSE           |      | 0            | Reversion de bits                                     |
| DATA_WIDTH        |      | 8            | Tamaño de los datos de entrada                        |
| STYLE             |      | "AUTO"       | Estilo de implementacion: "AUTO", "LOOP", "REDUCTION" |

## Ports

| Port name | Direction | Type                  | Description                                                         |
| --------- | --------- | --------------------- | ------------------------------------------------------------------- |
| data_in   | input     | wire [DATA_WIDTH-1:0] | Datos de entrada que se desplazarán a través del LFSR               |
| state_in  | input     | wire [LFSR_WIDTH-1:0] | Estado actual del LFSR                                              |
| data_out  | output    | wire [DATA_WIDTH-1:0] | Datos de salida que representan los bits desplazados fuera del LFSR |
| state_out | output    | wire [LFSR_WIDTH-1:0] | Próximo estado del LFSR                                             |

## Constants

| Name      | Type | Value                                   | Description                                        |
| --------- | ---- | --------------------------------------- | -------------------------------------------------- |
| STYLE_INT |      | (STYLE == "AUTO") ? "REDUCTION" : STYLE | "AUTO" style is "REDUCTION" for faster simulation  |
| STYLE_INT |      | (STYLE == "AUTO") ? "LOOP" : STYLE      | "AUTO" style is "LOOP" for better synthesis result |

## Functions
- lfsr_mask <font id="function_arguments">(input [31:0] index)</font> <font id="function_return">return ([LFSR_WIDTH+DATA_WIDTH-1:0])</font>
  - Funcion que calcula la máscara para la operación LFSR. Recibe un índice como entrada y devuelve una máscara de btis que se utiliza para seleccionar los bits relevantes para el cálculo del próximo estado