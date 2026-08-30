# Changelog — LEDS Text

Todos los cambios relevantes del proyecto se documentan en este archivo.

---

## [1.3.0] - 2026-08-30
### Added
- **Expansión de la Familia con Estilos Itálicos (5 Cursivas):** Diseño, transformación y exportación de 5 estilos itálicos en formatos OTF (`builds/otf/proof/`) y WOFF (`builds/woff/proof/`):
  - `LEDSTextLightItalic.otf` / `LEDSTextLightItalic.woff`
  - `LEDSTextRegularItalic.otf` / `LEDSTextRegularItalic.woff`
  - `LEDSTextMediumItalic.otf` / `LEDSTextMediumItalic.woff`
  - `LEDSTextSemiboldItalic.otf` / `LEDSTextSemiboldItalic.woff`
  - `LEDSTextBoldItalic.otf` / `LEDSTextBoldItalic.woff`
- **Paquete de Release Unificado:** Distribución oficial consolidada con los 10 estilos en formatos OTF y WOFF en `builds/release/LEDS_Text_v1.30.zip`.
- **Diseño y Transformación Cursiva:**
  - Ángulo de inclinación de 10° (`Slant: 10°`).
  - Descomposición y remoción de superposiciones en exportación (*Decompose & Remove Overlap*).
  - Variantes morfológicas cursivas para minúsculas: sustitución de glifos en exportación para `/a` (`a.001`), `/f` (`f.001`) y `/g` (`g.001`).
- **Vinculación de Estilos (*Style Linking*):**
  - Configuración completa de la cuádrupla base: `Regular` $\rightarrow$ `Bold` (**B**), `Regular` $\rightarrow$ `Regular Italic` (**I**), `Regular` $\rightarrow$ `Bold Italic` (**B+I**).
  - Vinculación de pares itálicos para `Light` $\leftrightarrow$ `Light Italic`, `Medium` $\leftrightarrow$ `Medium Italic` y `Semibold` $\leftrightarrow$ `Semibold Italic`.
- **Actualización de Versión de Metadatos:** Incremento a `v1.300` (`versionMajor = 1`, `versionMinor = 3`) en el archivo fuente de Glyphs.

### Fixed / Corrected
- **Corrección de Errores de Exportación:** Depuración de sintaxis y sustituciones de características OpenType (código de versalitas/Small Caps y reglas de ligaduras).
- **Actualización de Release:** Recompilación limpia y regeneración del paquete de distribución `LEDS_Text_v1.30.zip` con los binarios de producción corregidos.

### Changed / Optimized
- **Recompilación de la Familia Completa:** Generación sincronizada de los 10 estilos estáticos (5 Romanas + 5 Itálicas) en formatos OTF y WOFF.

### Font Metrics Summary
**Family Name:** "LEDS Text"
- **Units Per Em (UPM):** 1024
- **Number of Glyphs:** 380
- **Version:** 1.300; Glyphs 3.x
- **Italic Slant:** 10.0°

#### Styles Overview (10 Estilos)
- **Light (300) / Light Italic (300 Italic)**
- **Regular (400) / Regular Italic (400 Italic)**
- **Medium (500) / Medium Italic (500 Italic)**
- **Semibold (600) / Semibold Italic (600 Italic)**
- **Bold (700) / Bold Italic (700 Italic)**

---

## [1.2.0] - 2026-08-29
### Added
- **Compilación de Fuentes Web (WOFF):** Generación e incorporación de archivos en formato `.woff` para los 5 pesos en `builds/woff/proof/`:
  - `LEDSTextLight.woff`
  - `LEDSTextRegular.woff`
  - `LEDSTextMedium.woff`
  - `LEDSTextSemibold.woff`
  - `LEDSTextBold.woff`
- **Paquete de Release Unificado:** Distribución oficial consolidada con formatos OTF y WOFF en `builds/release/LEDS_Text_v1.20.zip`.

### Changed / Optimized
- **Optimización de Trazos y Nodos:** Limpieza de nodos duplicados y segmentos superpuestos de longitud cero en todas las capas de los glifos.
- **Recompilación OTF:** Generación y actualización de los binarios OTF (`builds/otf/proof/`) para los 5 pesos de la familia:
  - `LEDSTextLight.otf`
  - `LEDSTextRegular.otf`
  - `LEDSTextMedium.otf`
  - `LEDSTextSemibold.otf`
  - `LEDSTextBold.otf`

---

## [1.1.0] - 2026-03-04
### Added
- **Consolidación de Familia (5 Pesos Upright):** Homologación y compilación de 5 estilos (Light, Regular, Medium, Semibold y Bold).
- **Consolidación de Glifos:** Sincronización del set de 380 glifos en todos los estilos de la familia.
- **Soporte Lingüístico:** Validación del 100% de cobertura para 16 idiomas, incluyendo Checo, Finlandés, Galés e Irlandés.

### Fixed (Diagnóstico Fontbakery)
- **Estructura WWS (Weight, Width, Slope):** Corrección y asignación precisa de los valores de peso (300, 400, 500, 600, 700) en las tablas de metadatos.
- **Atributos de Selección (fsSelection):** Reparación de los bits de estilo en la tabla OS/2 para menús de software.
- **Validación de Soft Dotted:** Revisión de glifos con puntos suaves (como la /j) para asegurar el comportamiento correcto de desaparición del punto al combinar con diacríticos superiores.

### Font Metrics Summary
**Family Name:** "LEDS_Text"
- **Units Per Em (UPM):** 1024
- **Number of Glyphs:** 380
- **Version:** 1.100; Glyphs 3.5 (3509)

#### Styles Overview
- **Light (300)**
- **Regular (400):** Estilo base para vinculación.
- **Medium (500)**
- **Semibold (600)**
- **Bold (700):** Vinculado como estilo "Bold" de la familia.

---

## [1.0.4] - 2026-03-02
### Added
- **QA Testing:** Implementación de revisión con Fontbakery.
- Definición oficial de naming para la familia "LEDS Text".
- Registro estructural de los estilos Light (300), Regular (400), Medium (500), Semibold (600) y Bold (700).
- Incorporación de reporte de cobertura lingüística.
- Consolidación de métricas verticales compartidas.

### Fixed (Diagnóstico Fontbakery)
*Nota: Basado en el reporte `fontbakery-report.html` generado.*
- **Estructura de Contornos:** Identificación de nodos duplicados y componentes desalineados en el set de 380 glifos.
- **Naming:** Verificación de cadenas de texto en la tabla `name` para asegurar compatibilidad con instaladores de sistema.

### Font Metrics Summary
**Family Name:** "LEDS_Text"
- **Units Per Em (UPM):** 1024
- **Number of Glyphs:** 380
- **Version:** 1.000; Glyphs 3.5 (3509)

#### Styles Overview
- **Light (300)**
- **Regular (400):** Estilo base para vinculación.
- **Medium (500)**
- **Semibold (600)**
- **Bold (700):** Vinculado como estilo "Bold" de la familia.

---

## [0.1.0] - 2026-02-20
### Initial Technical Setup
- Configuración inicial de los parámetros del archivo fuente (Glyphs/UFO).

### Metrics (Setup inicial)
- **Italic Angle:** 0.0
- **Is Fixed Pitch:** 0
- **x-Height:** 430
- **Cap Height:** 638

### Vertical Metrics & Alignment Zones
| Type | Position (pos) |
| :--- | :--- |
| **Ascender** | 975 |
| **Cap Height** | 750 |
| **x-Height** | 500 |
| **Baseline** | 0 |
| **Descender** | -300 |
| **Italic Angle** | 0 |

---

## Language Coverage

### 100% (153 languages)
- Soporte completo para lenguas con sets latinos estándar y extendidos básicos, incluyendo:
- Español de México/América, Inglés (US), Italiano, Indonesio, Tagalo, Swahili, entre otras 147 lenguas adicionales del set Latin-1.

### 95% – 99%
Lenguas que requieren solo 1 o 2 glifos adicionales para soporte total:
- Spanish (Castellano): 98.63% (Falta /germandbls o uso de capitales específicas según contexto).
- Danish / Finnish / Norwegian / Swedish: ~98% (Falta /AE y /ae).
- Galician / Basque: ~98% (Faltan glifos de puntuación o variaciones raras).

### Medium Support (80% – 94%)
Requieren implementación de acentos específicos (Cedillas, Ogoneks, Hungarumlaut):
- German: 89.23% (Falta /germandbls).
- Hungarian: 90.67% (Faltan /Ohungarumlaut, /Uhungarumlaut y sus minúsculas).
- Turkish: 91.00% (Faltan /Idotaccent, /Scommaaccent).
- Polish / Lithuanian / Czech: ~85% (Faltan /Lslash, Ogoneks y Carons específicos).

### Partial Support (Below 70%)
Lenguas con sistemas de acentuación complejos o alfabetos no latinos:
- French: 68.18% (Falta el glifo /OE y /oe).
- Vietnamese: <20% (Falta el set completo de diacríticos combinados y /Dcroat).
- Cyrillic (Partial): Cobertura mínima (menos del 10%) en Bielorruso, Serbio y Bosnio.

### Missing Glyphs Priority (Para alcanzar 100% en lenguas principales)
Para mejorar drásticamente el soporte en Europa y América, se recomienda priorizar el dibujo de:
- Fundamentales: /AE, /ae, /OE, /oe, /germandbls.

Soporte Regional:
- Escandinavia/Islandia: /Eth, /eth, /Thorn, /thorn.
- Europa Central/Polonia: /Lslash, /lslash, /Aogonek, /Eogonek, /Iogonek, /Uogonek.
- Turquía/Rumania: /Idotaccent, /Scommaaccent, /scommaaccent, /Tcommaaccent, /tcommaaccent.
- Vietnamita: Requiere una expansión masiva de combinaciones de acentos (Breves, Circumflex y Horns con tonos).

---

### Notes
- Cobertura sólida en lenguas latinas occidentales.
- Cobertura parcial en Europa Central.
- Métricas verticales consistentes entre Regular y Bold.
