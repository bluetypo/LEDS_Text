# Nomenclatura — LEDS Text

Este documento define la estructura de metadatos y las convenciones de nomenclatura de la tabla `name` (especificación OpenType) para la familia tipográfica del **Laboratorio de Estructuras Sociales (LEDS)**, garantizando compatibilidad multiplataforma (macOS, Windows, Linux) y agrupamiento correcto en menús de aplicaciones.

---

## 1. Agrupamiento de Familia (Family Naming)

Para asegurar que los estilos aparezcan correctamente agrupados bajo una misma familia:

* **Family Name (ID 16 - Typographic Family Name):** `LEDS Text`
  - Nombre completo que agrupa a todos los estilos en menús extendidos.
* **Subfamily Name (ID 17 - Typographic Subfamily Name):** `Light` | `Regular` | `Medium` | `Semibold` | `Bold`
  - Identifica el peso individual de la fuente en menús extendidos.
* **Font Family Name (ID 1 - Family Name):** `LEDS Text`
  - Utilizado para compatibilidad en aplicaciones básicas.

---

## 2. Definición de Instancias (Styles & Weights)

La consistencia en la codificación de pesos se define a través de los valores de la tabla `OS/2` (`usWeightClass` y `usWidthClass`):

| Estilo / Peso | Style Name (ID 2/17) | Weight Class (`usWeightClass`) | Width Class (`usWidthClass`) |
| :--- | :--- | :---: | :---: |
| **Light** | Light | 300 | 5 (Medium) |
| **Regular** | Regular | 400 | 5 (Medium) |
| **Medium** | Medium | 500 | 5 (Medium) |
| **Semibold** | Semibold | 600 | 5 (Medium) |
| **Bold** | Bold | 700 | 5 (Medium) |

---

## 3. Vinculación de Estilos (Style Linking)

Para que el atajo de negrita (**B** / **Cmd+B**) funcione correctamente en software de oficina y diseño:

* **Par Base / Negrita:**
  - `Regular` + **B** $\rightarrow$ `Bold`

---

## 4. PostScript Name (ID 6) y Naming de Archivos

El nombre PostScript es fundamental para la generación de PDFs y la compatibilidad con RIPs de impresión. No debe superar los 29 caracteres, no contiene espacios y coincide con los nombres de archivo compilados:

* **Light:** `LEDSTextLight` $\rightarrow$ `LEDSTextLight.otf`
* **Regular:** `LEDSTextRegular` $\rightarrow$ `LEDSTextRegular.otf`
* **Medium:** `LEDSTextMedium` $\rightarrow$ `LEDSTextMedium.otf`
* **Semibold:** `LEDSTextSemibold` $\rightarrow$ `LEDSTextSemibold.otf`
* **Bold:** `LEDSTextBold` $\rightarrow$ `LEDSTextBold.otf`

---

## 5. Parámetros de Versión (ID 5)

* **Metadata de Versión (ID 5):** `Version 1.002; Glyphs 3.x`
* **Git Tags:** `v1.2.0`

---

## 6. Coherencia Institucional

En publicaciones oficiales del Laboratorio, la fuente debe referirse siempre como **LEDS Text**.
