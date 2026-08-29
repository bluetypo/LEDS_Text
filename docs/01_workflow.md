# Flujo de Trabajo Tipográfico (Workflow) — LEDS Text

Este documento describe el proceso recomendado para la edición, exportación, validación y publicación de la familia tipográfica **LEDS Text**.

## 1. Archivos de Diseño y Edición
* **Archivos Fuente Nivel de Diseño:** `sources/LEDS_Text.glyphs`, `sources/LEDS_Text 2.glyphs` y `sources/LEDS_tx-italic.glyphs`
* **Software de Edición:** Glyphs 3.x o superior.
* **Control de Masters:** La edición de formas, anclas y espaciado debe ejecutarse de forma consistente en el espacio de diseño para mantener la interpolación entre los distintos pesos e inclinaciones (Upright e Italic).

## 2. Exportación y Compilación de Instancias Estáticas
Las 10 instancias estáticas definidas en los archivos fuente se compilan en formato OpenType con curvas PostScript (OTF/CFF) y se ubican en:
* **Directorio de Prueba/Individual:** `builds/otf/proof/`
* **Directorio de Distribución (Release):** `builds/otf/release/`
* **Configuración de Exportación recomendada:**
  - Activar *Remove Overlaps* (Fusión de trazados superpuestos).
  - Activar *Autohinting* (Optimización de renderizado).
* **Nombres de Archivo Oficiales (PostScript Names):**
  - **Light:** `LEDSText-Ligth.otf` / `LEDSText-Ligthitalic.otf`
  - **Regular:** `LEDSText-Regular.otf` / `LEDSText-Regularitalic.otf`
  - **Medium:** `LEDSText-Medium.otf` / `LEDSText-MediumItalic.otf`
  - **SemiBold:** `LEDSText-Semibold.otf` / `LEDSText-SemiboldItalic.otf`
  - **Bold:** `LEDSText-Bold.otf` / `LEDSText-BoldItalic.otf`

## 3. Pruebas de QA y Diagnóstico (Fontbakery)
Antes de empaquetar una release de producción:
1. Ejecutar las pruebas de diagnóstico con Fontbakery sobre las fuentes compiladas en `builds/otf/proof/`.
2. Verificar la integridad de metadatos WWS (Weight, Width, Slope) y la correcta configuración de atributos de selección (`fsSelection`).
3. Guardar los reportes de calidad en `tests/fontbakery/`.

## 4. Publicación y Distribución Oficial (Releases)
Una vez que las instancias estáticas han superado las pruebas de calidad de métricas, rendering y Style Linking:
1. Empaqueta los archivos OTF finales en un archivo comprimido `.zip` (`LEDS_Text_v1.10.zip`), incluyendo el archivo de documentación y EULA correspondiente.
2. Guarda el paquete oficial en: `builds/otf/release/`.
3. Actualiza el historial en el archivo `CHANGELOG.md` de la raíz del proyecto.
4. Genera la etiqueta correspondiente en Git (ej. `git tag -a v1.1.0`) y haz push a GitHub.
