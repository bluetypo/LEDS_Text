# Changelog — LEDS_Text

Todos los cambios relevantes del proyecto se documentan en este archivo.

---

## [1.1.0] - 2026-03-04
### Added
- **Expansión de Familia:** Incorporación de 5 nuevos estilos Itálicos (Light, Regular, Medium, Semibold y Bold).
- **Consolidación de Glifos:** Sincronización del set de 380 glifos en todos los estilos de la familia (10 fuentes en total).
- **Soporte Lingüístico:** Validación del 100% de cobertura para 16 idiomas, incluyendo Checo, Finlandés, Galés e Irlandés en toda la familia.

### Fixed (Diagnóstico Fontbakery)
*Nota: Basado en el reporte de conflictos de pesos y metadatos de la nueva vertiente.*
- **Estructura WWS (Weight, Width, Slope):** Corrección del error donde los estilos itálicos reportaban un peso erróneo de 400. Se asignaron los valores correctos (300, 500, 600, 700) en las tablas de metadatos.
- **Atributos de Selección (fsSelection):** Reparación de los bits de estilo para asegurar que el sistema diferencie correctamente entre las variantes Romanas y Cursivas en los menús de software.
- **Validación de Soft Dotted:** Revisión de glifos con puntos suaves (como la /j) para asegurar el comportamiento correcto de desaparición del punto al combinar con diacríticos superiores.

### Font Metrics Summary
**Family Name:** "LEDS_Text"
- **Units Per Em (UPM):** 1024
- **Number of Glyphs:** 380
- **Version:** 1.100; Glyphs 3.5 (3509)

#### Styles Overview
- **Light (300) / Light Italic (300)**
- **Regular (400) / Regular Italic (400):** Estilos base para vinculación.
- **Medium (500) / Medium Italic (500)**
- **Semibold (600) / Semibold Italic (600)**
- **Bold (700) / Bold Italic (700):** Vinculados como estilos "Bold" de la familia.

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
