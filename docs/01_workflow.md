# Flujo de Trabajo Tipográfico (Workflow) — LEDS Text

Este documento describe el proceso recomendado para la edición, exportación, validación y publicación de la familia tipográfica **LEDS Text**.

## 1. Archivo de Diseño y Edición
* **Archivo Fuente Nivel de Diseño:** `sources/LEDS_Text.glyphs`
* **Software de Edición:** Glyphs 3.x o superior.
* **Control de Masters:** La edición de formas, anclas y espaciado debe ejecutarse de forma consistente en el espacio de diseño para mantener la compatibilidad de interpolación entre los 5 pesos Upright (Light, Regular, Medium, Semibold y Bold).

## 2. Exportación y Compilación de Instancias Estáticas
Las 5 instancias estáticas definidas en el archivo fuente se compilan en formatos OpenType (OTF/CFF) y Web (WOFF), ubicándose en:
* **Directorio de Prueba/Individual OTF:** `builds/otf/proof/`
* **Directorio de Prueba/Individual WOFF:** `builds/woff/proof/`
* **Directorio de Distribución (Release):** `builds/release/`
* **Configuración de Exportación recomendada:**
  - Activar *Remove Overlaps* (Fusión de trazados superpuestos).
  - Activar *Autohinting* (Optimización de renderizado).
* **Nombres de Archivo Oficiales (PostScript Names):**
  - **Light:** `LEDSTextLight.otf` / `LEDSTextLight.woff` (`LEDSTextLight`)
  - **Regular:** `LEDSTextRegular.otf` / `LEDSTextRegular.woff` (`LEDSTextRegular`)
  - **Medium:** `LEDSTextMedium.otf` / `LEDSTextMedium.woff` (`LEDSTextMedium`)
  - **SemiBold:** `LEDSTextSemibold.otf` / `LEDSTextSemibold.woff` (`LEDSTextSemibold`)
  - **Bold:** `LEDSTextBold.otf` / `LEDSTextBold.woff` (`LEDSTextBold`)

## 3. Pruebas de QA y Diagnóstico (Fontbakery)
Antes de empaquetar una release de producción:
1. Ejecutar las pruebas de diagnóstico con Fontbakery sobre las fuentes compiladas en `builds/otf/proof/`.
2. Verificar la integridad de metadatos WWS (Weight, Width, Slope) y la correcta configuración de atributos de selección (`fsSelection`).
3. Guardar los reportes de calidad en `tests/fontbakery/`.

## 4. Publicación y Distribución Oficial (Releases)
Una vez que las instancias estáticas han superado las pruebas de calidad de métricas, rendering y Style Linking:
1. Empaqueta los archivos OTF y WOFF finales en un archivo comprimido `.zip` (`LEDS_Text_v1.20.zip`), incluyendo el archivo de documentación y EULA correspondiente.
2. Guarda el paquete oficial en: `builds/release/`.
3. Actualiza el historial en el archivo `CHANGELOG.md` de la raíz del proyecto.
4. Genera la etiqueta correspondiente en Git (ej. `git tag -a v1.2.0`) y haz push a GitHub.
