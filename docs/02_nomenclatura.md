# Nomenclatura — LEDS Text

Este documento define la estructura de metadatos y las convenciones de nomenclatura de la tabla `name` (especificación OpenType) para la familia tipográfica del **Laboratorio de Estructuras Sociales (LEDS)**, garantizando compatibilidad multiplataforma (macOS, Windows, Linux) y agrupamiento correcto en menús de aplicaciones.

---

## 1. Agrupamiento de Familia (Family Naming)

Para evitar problemas de fragmentación en los menús y asegurar que los 10 estilos aparezcan agrupados bajo una misma familia:

* **Family Name (ID 16 - Typographic Family Name):** `LEDS Text`
  - Nombre completo que agrupa a todos los estilos en menús extendidos.
* **Subfamily Name (ID 17 - Typographic Subfamily Name):** `Light` | `Light Italic` | `Regular` | `Regular Italic` | `Medium` | `Medium Italic` | `Semibold` | `Semibold Italic` | `Bold` | `Bold Italic`
  - Identifica el peso e inclinación individual de la fuente en menús extendidos.
* **Font Family Name (ID 1 - Family Name):** `LEDS Text`
  - Utilizado para compatibilidad en aplicaciones básicas que solo admiten el modelo de cuatro estilos (Regular, Italic, Bold, Bold Italic).

---

## 2. Definición de Instancias (Styles & Weights)

La consistencia en la codificación de pesos se define a través de los valores de la tabla `OS/2` (`usWeightClass` y `usWidthClass`):

| Estilo / Peso | Style Name (ID 2/17) | Weight Class (`usWeightClass`) | Width Class (`usWidthClass`) |
| :--- | :--- | :---: | :---: |
| **Light** | Light / Light Italic | 300 | 5 (Medium) |
| **Regular** | Regular / Regular Italic | 400 | 5 (Medium) |
| **Medium** | Medium / Medium Italic | 500 | 5 (Medium) |
| **Semibold** | Semibold / Semibold Italic | 600 | 5 (Medium) |
| **Bold** | Bold / Bold Italic | 700 | 5 (Medium) |

---

## 3. Vinculación de Estilos (Style Linking)

Para que los atajos de negrita (**B** / **Cmd+B**) e itálica (**I** / **Cmd+I**) funcionen correctamente en software de oficina y diseño:

* **Pares Base / Negrita / Itálica:**
  - `Regular` + **B** $\rightarrow$ `Bold`
  - `Regular` + **I** $\rightarrow$ `Regular Italic`
  - `Regular` + **B** + **I** $\rightarrow$ `Bold Italic`
* **Estilos adicionales (Light, Medium, Semibold):**
  - Cada variante Upright se vincula a su correspondiente variante **Italic** mediante el atajo **I** / **Cmd+I**.

---

## 4. PostScript Name (ID 6) y Naming de Archivos

El nombre PostScript es fundamental para la generación de PDFs y la compatibilidad con RIPs de impresión. No debe superar los 29 caracteres, no contiene espacios y coincide con los nombres de archivo compilados:

* **Light:** `LEDSText-Ligth` $\rightarrow$ `LEDSText-Ligth.otf` / `LEDSText-Ligthitalic` $\rightarrow$ `LEDSText-Ligthitalic.otf`
* **Regular:** `LEDSText-Regular` $\rightarrow$ `LEDSText-Regular.otf` / `LEDSText-Regularitalic` $\rightarrow$ `LEDSText-Regularitalic.otf`
* **Medium:** `LEDSText-Medium` $\rightarrow$ `LEDSText-Medium.otf` / `LEDSText-MediumItalic` $\rightarrow$ `LEDSText-MediumItalic.otf`
* **Semibold:** `LEDSText-Semibold` $\rightarrow$ `LEDSText-Semibold.otf` / `LEDSText-SemiboldItalic` $\rightarrow$ `LEDSText-SemiboldItalic.otf`
* **Bold:** `LEDSText-Bold` $\rightarrow$ `LEDSText-Bold.otf` / `LEDSText-BoldItalic` $\rightarrow$ `LEDSText-BoldItalic.otf`

---

## 5. Parámetros de Versión (ID 5)

* **Metadata de Versión (ID 5):** `Version 1.100; Glyphs 3.x`
* **Git Tags:** `v1.1.0`

---

## 6. Coherencia Institucional

En publicaciones oficiales del Laboratorio, la fuente debe referirse siempre como **LEDS Text**.
