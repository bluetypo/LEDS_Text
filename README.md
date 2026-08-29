# LEDS Text

![LEDS Text Specimen](assets/LEDS_Text.png)

**LEDS Text** es la familia tipográfica oficial del **Laboratorio de Estructuras Sociales (LEDS)**, perteneciente a la Facultad del Hábitat de la Universidad Autónoma de San Luis Potosí (UASLP).

Este repositorio aloja los archivos fuente de diseño y las compilaciones de producción de la familia, estructurados bajo estándares profesionales de desarrollo tipográfico y control de versiones.

## Estructura de la Familia (10 Estilos - Release v1.1.0)
La familia compilada en producción se compone de **5 pesos** con sus correspondientes variantes **Upright** (Romana) e **Italic** (Cursiva), sumando un total de **10 instancias estáticas** disponibles en formato **OTF** (Desktop):

| Estilo / Instancia | Upright | Italic | Weight Class | Archivos (OTF) | PostScript Name |
| :--- | :---: | :---: | :---: | :--- | :--- |
| **Light** | ✓ | ✓ | 300 | `LEDSText-Ligth.otf`<br>`LEDSText-Ligthitalic.otf` | `LEDSText-Ligth`<br>`LEDSText-Ligthitalic` |
| **Regular** | ✓ | ✓ | 400 | `LEDSText-Regular.otf`<br>`LEDSText-Regularitalic.otf` | `LEDSText-Regular`<br>`LEDSText-Regularitalic` |
| **Medium** | ✓ | ✓ | 500 | `LEDSText-Medium.otf`<br>`LEDSText-MediumItalic.otf` | `LEDSText-Medium`<br>`LEDSText-MediumItalic` |
| **SemiBold** | ✓ | ✓ | 600 | `LEDSText-Semibold.otf`<br>`LEDSText-SemiboldItalic.otf` | `LEDSText-Semibold`<br>`LEDSText-SemiboldItalic` |
| **Bold** | ✓ | ✓ | 700 | `LEDSText-Bold.otf`<br>`LEDSText-BoldItalic.otf` | `LEDSText-Bold`<br>`LEDSText-BoldItalic` |

## Especificaciones Técnicas (Font Specs)
* **Formatos de Distribución:**
  * **Desktop / Print:** OpenType CFF (`.otf`) compilado con curvas PostScript (cúbicas).
* **Ubicación de Compilación y Release:** [`builds/otf/release/`](builds/otf/release/) (paquetes `.zip`), [`builds/otf/proof/`](builds/otf/proof/) (`.otf`).
* **Unidades por Em (UPM):** 1024.
* **Set de Glifos por Archivo:** 380 glifos (cobertura Latin extendida con diacríticos, versalitas y ligaduras).
* **OpenType Features (GSUB):** 
  * `aalt` — *Access All Alternates*
  * `case` — *Case-Sensitive Forms*
  * `ccmp` — *Glyph Composition/Decomposition*
  * `liga` — *Standard Ligatures*
  * `locl` — *Localized Forms*
* **Soporte Lingüístico:** Cobertura de 153 lenguas con base latina (100% de cobertura en 16 lenguas clave como Checo, Finlandés, Galés, Irlandés y Español).

## Estado de Producción
Las **10 instancias estáticas** en formato **OTF** listas para distribución se ubican en:
* [`builds/otf/release/`](builds/otf/release/) — Paquetes oficiales de distribución (`LEDS_Text_v1.10.zip`), incluyendo documentación interna (`CHANGELOG.md` y `EULA_LEDS_Text.txt`).
* [`builds/otf/proof/`](builds/otf/proof/) — Archivos binarios individuales `.otf`.

Los archivos fuente máster en formato Glyphs (`sources/LEDS_Text 2.glyphs`, `sources/LEDS_Text.glyphs` y `sources/LEDS_tx-italic.glyphs`) se encuentran estructurados en [`sources/`](sources/) para facilitar el mantenimiento y la compilación de futuras versiones.

## Sobre el Laboratorio
El Laboratorio de Estructuras Sociales (LEDS) es un espacio de investigación y análisis enfocado en articular el diseño gráfico contemporáneo con la tecnología y las estructuras sociales.
🌐 [Visita el sitio oficial del Laboratorio de Estructuras Sociales](https://leds.uaslp.mx)

---

## Pruebas de Rendering y QA
1. Descarga las fuentes compiladas desde [`builds/otf/release/`](builds/otf/release/) o explora las versiones individuales en [`builds/otf/proof/`](builds/otf/proof/).
2. **Fuentes Desktop (OTF):** Instala los archivos `.otf` en tu sistema operativo o gestor de fuentes y valida la vinculación de estilos (*Style Linking*) con los atajos de teclado (**B** / **N** para negritas y **I** / **K** para itálicas).
3. **Pruebas de Calidad:** Las validaciones de metadatos y contornos se ejecutan mediante *Fontbakery* y se registran en [`tests/fontbakery/`](tests/fontbakery/).

## Licencia y EULA
Esta tipografía se distribuye bajo la licencia abierta **SIL Open Font License 1.1** detallada en el archivo [LICENSE.txt](LICENSE.txt). Puedes consultar los términos de uso y derechos de distribución en el [Acuerdo de Licencia de Usuario Final (EULA.md)](EULA.md).
