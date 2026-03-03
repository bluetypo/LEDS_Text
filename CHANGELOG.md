# Changelog — Esperanza Sans

Todos los cambios relevantes del proyecto se documentan en este archivo.

---

## [Unreleased]
### Added
-
### Changed
-
### Fixed
-

---


## [0.1.0] - 2026-03-02
### Initial Technical Setup
Configuración inicial de los parámetros del archivo fuente (Glyphs/UFO).

### Metrics (aplicable a todos los estilos)
- **Number of Glyphs:** 380
- **Units Per Em (UPM):** 1024
- **Italic Angle:** 0.0
- **Is Fixed Pitch:** 0
- **Weight Class:** 400 (Regular)
- **Width Class:** 5 (Medium/Normal)
- **x-Height:** 430
- **Cap Height:** 638

### Vertical Metrics & Alignment Zones
Configuración definida en el archivo de diseño:

| Type | Position (pos) |
| :--- | :--- |
| **Ascender** | 975 |
| **Cap Height** | 750 |
| **x-Height** | 500 |
| **Baseline** | 0 |
| **Descender** | -300 |
| **Italic Angle** | 0 |

> **Nota técnica:** Se observa una discrepancia intencional entre la métrica general de `Cap Height (638)` y la zona de alineación `pos = 750`. Esto será revisado en la próxima sesión de dibujo para ajuste de overshoot.

---

## Family Charset Overview

- LEDS Text Light (300): 380 glyphs
- LEDS Text Regular (400): 380 glyphs
- LEDS Text Medium (500): 380 glyphs
- LEDS Text Semibold (600): 380 glyphs
- LEDS Text Bold (700): 380 glyphs

---

### Notes
- Incremento de 128 a 380 glifos en todos los estilos.
- Mejora en la consistencia del ritmo visual entre estilos.
- Ajustes enfocados en equilibrio de blancos y homogeneidad del gris tipográfico.
- Preparación para pruebas finales de impresión y validación editorial.

---

## [1.0.4] - 2026-02-11

### Added
- Definición oficial de naming para la familia "LEDS Text".
- Registro estructural de los estilos Light (300), Regular (400), Medium (500), Semibold (600) y Bold (700).
- Incorporación de reporte de cobertura lingüística.
- Consolidación de métricas verticales compartidas.

---

## Font

**Family Name:** "LEDS_Text"

### Regular
- Style Name: "Regular"
- Style Linking Family: "LEDS Text"
- Style Linking Style: "Regular"

### Bold
- Style Name: "Bold"
- Style Linking Family: "LEDS Text"
- Style Linking Style: "Bold"

- Version string:
  - "Version 1.000; Glyphs 3.5 (3509)"

---

## Metrics



---

## Language Coverage

### 100%
- Irish (67/67)
- Latin0 (57/57)

### 95% – 99%
- Spanish: 98.63% (72/73)
- Galician: 98.59% (70/71)
- Basque: 98.36% (60/61)

### 85% – 94%
- Albanian: 93.44% (57/61)
- Hungarian: 90.67% (68/75)
- Danish: 90.48% (57/63)
- Finnish: 90.48% (57/63)
- German: 89.23% (58/65)
- Faroese: 89.04% (65/73)
- Icelandic: 87.01% (67/77)
- Bosnian (LAT): 85.07% (57/67)
- Croatian: 85.07% (57/67)
- Italian: 85.07% (57/67)
- Romanian: 85.07% (57/67)
- Estonian: 84.06% (58/69)
- Swedish: 84.93% (62/73)
- Catalan: 83.54% (66/79)
- Guarani: 83.10% (59/71)
- Esperanto: 82.61% (57/69)
- Breton: 82.19% (60/73)

### 70% – 84%
- Polish: 78.67% (59/75)
- Portuguese: 78.82% (67/85)
- Czech: 77.01% (67/87)
- Afrikaans: 77.33% (58/75)
- Lithuanian: 76.00% (57/75)
- Dutch: 76.40% (68/89)
- Norwegian: 75.29% (64/85)
- Maltese: 74.03% (57/77)
- Slovak: 73.63% (67/91)
- Slovenian: 79.45% (58/73)

### Below 70%
- French: 68.18% (60/88)
- Latvian: 66.67% (44/66)
- Welsh: 60.18% (68/113)

### Cyrillic (Partial Coverage)
- Belarusian: 7.89% (6/76)
- Bosnian (CYR): 7.69% (5/65)
- Serbian: 9.09% (6/66)

---

### Notes
- Cobertura sólida en lenguas latinas occidentales.
- Cobertura parcial en Europa Central.
- Métricas verticales consistentes entre Regular y Bold.
