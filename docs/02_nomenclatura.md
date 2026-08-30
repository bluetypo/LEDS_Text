# Nomenclatura — LEDS Text

Este documento define la estructura de metadatos y las convenciones de nomenclatura de la tabla `name` (especificación OpenType) para la familia tipográfica del **Laboratorio de Estructuras Sociales (LEDS)**, garantizando compatibilidad multiplataforma (macOS, Windows, Linux) y agrupamiento correcto en menús de aplicaciones.

---

## 1. Agrupamiento de Familia (Family Naming)

Para asegurar que los estilos aparezcan correctamente agrupados bajo una misma familia:

* **Family Name (ID 16 - Typographic Family Name):** `LEDS Text`
  - Nombre completo que agrupa a los 10 estilos en menús extendidos.
* **Subfamily Name (ID 17 - Typographic Subfamily Name):**  
  `Light` | `Light Italic` | `Regular` | `Regular Italic` | `Medium` | `Medium Italic` | `Semibold` | `Semibold Italic` | `Bold` | `Bold Italic`
  - Identifica el peso e inclinación individual de la fuente en menús extendidos.
* **Font Family Name (ID 1 - Family Name):** `LEDS Text`
  - Utilizado para compatibilidad en aplicaciones básicas y vinculación de 4 estilos (*RIBBI*).

---

## 2. Definición de Instancias (Styles, Weights & Slope)

La consistencia en la codificación de pesos se define a través de los valores de la tabla `OS/2` (`usWeightClass`, `usWidthClass` y `fsSelection`):

| Estilo / Instancia | Typographic Subfamily (ID 17) | Weight Class (`usWeightClass`) | Width Class (`usWidthClass`) | Is Italic | Is Bold |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **Light** | Light | 300 | 5 (Medium) | No | No |
| **Light Italic** | Light Italic | 300 | 5 (Medium) | Sí | No |
| **Regular** | Regular | 400 | 5 (Medium) | No | No |
| **Regular Italic** | Regular Italic | 400 | 5 (Medium) | Sí | No |
| **Medium** | Medium | 500 | 5 (Medium) | No | No |
| **Medium Italic** | Medium Italic | 500 | 5 (Medium) | Sí | No |
| **Semibold** | Semibold | 600 | 5 (Medium) | No | No |
| **Semibold Italic** | Semibold Italic | 600 | 5 (Medium) | Sí | No |
| **Bold** | Bold | 700 | 5 (Medium) | No | Sí |
| **Bold Italic** | Bold Italic | 700 | 5 (Medium) | Sí | Sí |

---

## 3. Vinculación de Estilos (Style Linking)

Para que los atajos de negrita (**B** / **Cmd+B**) e itálica (**I** / **Cmd+I**) funcionen de forma natural y robusta en software de oficina y diseño:

* **Cuádrupla Base (RIBBI Grouping):**
  - Base: `Regular`
  - Negrita (**B**): `Bold`
  - Cursiva (**I**): `Regular Italic`
  - Negrita + Cursiva (**B + I**): `Bold Italic`

* **Pares Vinculados Adicionales:**
  - `Light` + **I** $\rightarrow$ `Light Italic`
  - `Medium` + **I** $\rightarrow$ `Medium Italic`
  - `Semibold` + **I** $\rightarrow$ `Semibold Italic`

---

## 4. PostScript Name (ID 6) y Naming de Archivos

El nombre PostScript es fundamental para la generación de PDFs y la compatibilidad con RIPs de impresión. No supera los 29 caracteres, no contiene espacios y coincide con los nombres de archivo compilados en formatos Desktop (`.otf`) y Web (`.woff`):

* **Light:** `LEDSTextLight` $\rightarrow$ `LEDSTextLight.otf` / `LEDSTextLight.woff`
* **Light Italic:** `LEDSTextLightItalic` $\rightarrow$ `LEDSTextLightItalic.otf` / `LEDSTextLightItalic.woff`
* **Regular:** `LEDSTextRegular` $\rightarrow$ `LEDSTextRegular.otf` / `LEDSTextRegular.woff`
* **Regular Italic:** `LEDSTextRegularItalic` $\rightarrow$ `LEDSTextRegularItalic.otf` / `LEDSTextRegularItalic.woff`
* **Medium:** `LEDSTextMedium` $\rightarrow$ `LEDSTextMedium.otf` / `LEDSTextMedium.woff`
* **Medium Italic:** `LEDSTextMediumItalic` $\rightarrow$ `LEDSTextMediumItalic.otf` / `LEDSTextMediumItalic.woff`
* **Semibold:** `LEDSTextSemibold` $\rightarrow$ `LEDSTextSemibold.otf` / `LEDSTextSemibold.woff`
* **Semibold Italic:** `LEDSTextSemiboldItalic` $\rightarrow$ `LEDSTextSemiboldItalic.otf` / `LEDSTextSemiboldItalic.woff`
* **Bold:** `LEDSTextBold` $\rightarrow$ `LEDSTextBold.otf` / `LEDSTextBold.woff`
* **Bold Italic:** `LEDSTextBoldItalic` $\rightarrow$ `LEDSTextBoldItalic.otf` / `LEDSTextBoldItalic.woff`

---

## 5. Parámetros de Versión (ID 5)

* **Metadata de Versión (ID 5):** `Version 1.003; Glyphs 3.x`
* **Git Tags:** `v1.3.0`

---

## 6. Coherencia Institucional

En publicaciones oficiales del Laboratorio, la fuente debe referirse siempre como **LEDS Text**.
