# Nomenclatura — LEDS_Text

Este documento define las convenciones oficiales de naming para la familia tipográfica del **Laboratorio de Estructuras Sociales**.

Su objetivo es garantizar coherencia entre:
- Metadata interna (Font Info / Tabla `name`)
- Archivos exportados (.otf, .woff2)
- Compatibilidad en sistemas operativos (Windows / macOS)
- Estructura del repositorio y comunicación del LEDS.

---

## 1. Family Name

**Family Name oficial:** `LEDS Text` (para visualización en menús)  
`LEDS_Text` (para nombres de archivo y PostScript)

Este nombre debe mantenerse idéntico en todos los estilos para asegurar el agrupamiento correcto.

---

## 2. Style Names & Metrics

| Estilo      | Style Name | Weight Class | Width Class |
|-------------|------------|--------------|-------------|
| **Light** | Light      | 300          | 5 (Medium)  |
| **Regular** | Regular    | 400          | 5 (Medium)  |
| **Medium** | Medium     | 500          | 5 (Medium)  |
| **Semibold** | Semibold   | 600          | 5 (Medium)  |
| **Bold** | Bold       | 700          | 5 (Medium)  |

---

## 3. Style Linking (Vinculación de Estilos)

Para asegurar que el uso de las teclas rápidas (**B** / **I**) funcione correctamente en software de oficina y diseño:

**Regular (Base):**
- Style Linking Family: `LEDS Text`
- Style Linking Style: `Regular`

**Bold:**
- Style Linking Family: `LEDS Text`
- Style Linking Style: `Bold` (Vinculado al Regular)

**Light / Medium / Semibold:**
- Estos estilos no suelen llevar vinculación de estilo (Style Linking) para evitar conflictos en menús de aplicaciones básicas, a menos que se definan parejas específicas.

---

## 4. Naming para exportación (Archivos)

Formato oficial sin espacios para evitar errores en servidores y código:

- `LEDS_Text-Light.otf`
- `LEDS_Text-Regular.otf`
- `LEDS_Text-Medium.otf`
- `LEDS_Text-Semibold.otf`
- `LEDS_Text-Bold.otf`

**Reglas:**
- Sin versiones en el nombre del archivo (ej. NO usar `LEDS_Text_v1.otf`).
- La versión se controla exclusivamente mediante el `CHANGELOG.md` y la metadata interna.

---

## 5. Versionado

**Formato interno (Metadata):** `Version 1.000; Glyphs 3.5 (3509)`

**Convención de versión en Repositorio (Git Tags):** - `v1.0.4` (Versión actual de producción)
- `v1.1.0` (Siguiente hito de glifos)

---

## 6. PostScript Name (PS Name)

El nombre PostScript es crítico para la impresión y generación de PDF. No debe exceder los 29 caracteres y no debe contener espacios:

- `LEDSText-Light`
- `LEDSText-Regular`
- `LEDSText-Medium`
- `LEDSText-Semibold`
- `LEDSText-Bold`

---

## 7. Futuras extensiones (Italics)

Cuando se incorporen las itálicas (actualmente en `sources/italic/`), se seguirá este patrón:

- **Style Name:** `Italic` / `Bold Italic`
- **PostScript:** `LEDSText-Italic` / `LEDSText-BoldItalic`
- **Style Linking:** El estilo `Italic` se vinculará al `Regular`, y el `Bold Italic` al `Bold`.

---

## 8. Coherencia Institucional

En publicaciones del Laboratorio, la fuente debe referirse siempre como **LEDS Text**.

Cualquier variante experimental o histórica (como los archivos en `sources/Bold_export/`) debe mantenerse fuera de las carpetas de `builds/` para evitar confusiones en la implementación final del laboratorio.
