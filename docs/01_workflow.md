# Flujo de Trabajo Tipográfico (Workflow) — LEDS Text

Este documento describe el proceso recomendado para la edición, exportación, validación y publicación de la familia tipográfica **LEDS Text**.

## 1. Archivo de Diseño y Edición
* **Archivo Fuente Nivel de Diseño:** `sources/LEDS_Text.glyphs`
* **Software de Edición:** Glyphs 3.x o superior.
* **Control de Masters e Interpolación:** La edición de formas, anclas y espaciado se gestiona en los masters del espacio de diseño, interpolando los 5 pesos principales (Light, Regular, Medium, Semibold y Bold) y derivando las variantes itálicas mediante parámetros customizados de exportación.

## 2. Exportación y Compilación de Instancias Estáticas
Las **10 instancias estáticas** (5 Romanas y 5 Itálicas) se compilan en formatos OpenType (OTF/CFF) y Web (WOFF), ubicándose en:
* **Directorio de Prueba/Individual OTF:** `builds/otf/proof/`
* **Directorio de Prueba/Individual WOFF:** `builds/woff/proof/`
* **Directorio de Distribución (Release):** `builds/release/`
* **Configuración de Exportación:**
  - **Instancias Romanas (Upright):** PreFiltro *RemoveOverlap*.
  - **Instancias Itálicas:** PreFiltro *Decompose* + *RemoveOverlap*, Filtro de Transformación de Inclinación `Slant:10` y regla de reemplazo de glifos cursivos (*Rename Glyphs*: `a=a.001`, `f=f.001`, `g=g.001`).
* **Nombres de Archivo Oficiales (PostScript Names):**
  - **Light:** `LEDSTextLight.otf` / `LEDSTextLight.woff` (`LEDSTextLight`)
  - **Light Italic:** `LEDSTextLightItalic.otf` / `LEDSTextLightItalic.woff` (`LEDSTextLightItalic`)
  - **Regular:** `LEDSTextRegular.otf` / `LEDSTextRegular.woff` (`LEDSTextRegular`)
  - **Regular Italic:** `LEDSTextRegularItalic.otf` / `LEDSTextRegularItalic.woff` (`LEDSTextRegularItalic`)
  - **Medium:** `LEDSTextMedium.otf` / `LEDSTextMedium.woff` (`LEDSTextMedium`)
  - **Medium Italic:** `LEDSTextMediumItalic.otf` / `LEDSTextMediumItalic.woff` (`LEDSTextMediumItalic`)
  - **SemiBold:** `LEDSTextSemibold.otf` / `LEDSTextSemibold.woff` (`LEDSTextSemibold`)
  - **SemiBold Italic:** `LEDSTextSemiboldItalic.otf` / `LEDSTextSemiboldItalic.woff` (`LEDSTextSemiboldItalic`)
  - **Bold:** `LEDSTextBold.otf` / `LEDSTextBold.woff` (`LEDSTextBold`)
  - **Bold Italic:** `LEDSTextBoldItalic.otf` / `LEDSTextBoldItalic.woff` (`LEDSTextBoldItalic`)

## 3. Pruebas de QA y Diagnóstico (Fontbakery)
Antes de empaquetar una release de producción:
1. Ejecutar las pruebas de diagnóstico con Fontbakery sobre las fuentes compiladas en `builds/otf/proof/`.
2. Verificar la integridad de metadatos WWS (Weight, Width, Slope) y la correcta configuración de atributos de selección (`fsSelection` / bits Bold e Italic).
3. Validar el funcionamiento del *Style Linking* (atajos **B**, **I** y **B+I**).
4. Guardar los reportes de calidad en `tests/fontbakery/`.

## 4. Publicación y Distribución Oficial (Releases)
Una vez que las instancias estáticas han superado las pruebas de calidad de métricas, rendering y Style Linking:
1. Empaqueta los archivos OTF y WOFF finales en un archivo comprimido `.zip`, incluyendo la documentación (`CHANGELOG.md` y `EULA.md`).
2. Guarda el paquete oficial en: `builds/release/`.
3. Actualiza el historial en el archivo `CHANGELOG.md` de la raíz del proyecto y en `docs/03_releases.md`.
4. Genera la etiqueta correspondiente en Git (ej. `git tag -a v1.3.0`) y haz push a GitHub.
