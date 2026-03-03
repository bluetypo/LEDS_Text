# Changelog — LEDS_Text

Todos los cambios relevantes del proyecto se documentan en este archivo.

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

## Language Coverage (v1.0.4)

### 100%
- Irish (67/67), Latin0 (57/57).

### High Priority Coverage (95% – 99%)
- **Spanish:** 98.63% (Faltan glifos específicos de puntuación o acentuación regional).
- Galician: 98.59%, Basque: 98.36%.

### 70% – 94% (Soporte extendido)
- Cobertura sólida en lenguas latinas occidentales (Italiano, Alemán, Portugués).
- Cobertura parcial en Europa Central (Polaco, Checo, Eslovaco).

---

### Notes
- **Expansión:** Incremento de 128 a 380 glifos en todos los estilos.
- **Calidad:** El reporte de Fontbakery indica que se debe prestar atención al "roundtrip" de los archivos binarios si se compilan en entornos web, recomendando la compilación local para evitar errores estructurales.
- **Objetivo:** Preparación para validación editorial y pruebas de impresión en el Laboratorio.
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
