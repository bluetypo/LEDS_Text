# Registro de Releases — LEDS Text

Este archivo documenta la hoja de ruta (*roadmap*), lanzamientos de producción e hitos técnicos en la vida del proyecto tipográfico **LEDS Text**.

---

## [v1.1.0] - 2026-03-04 (Actual)
**Estado:** Estable / Compilación de Producción  
**Estilos:** Light, Regular, Medium, Semibold, Bold (5 pesos en versión Upright).  
**Enfoque:** Lanzamiento consolidado de la familia romana en 5 pesos en formato OTF empaquetados en `builds/otf/release/`.

### Hitos Técnicos:
- Compilación de 5 estilos estáticos en formato OTF (Light, Regular, Medium, Semibold, Bold).
- Sincronización del set de 380 glifos en todos los estilos romanos.
- Corrección y validación de metadatos WWS (Weight, Width, Slope) e inspección con Fontbakery.
- Configuración de la estructura del repositorio de desarrollo y documentación homologada para Git.

---

## Próximos Lanzamientos Planificados (Roadmap)

### [v1.2.0] - Fecha TBD
**Enfoque:** Construcción e Integración de Itálicas (Cursivas) y Fuentes Web (WOFF / WOFF2)
- Desarrollo y dibujo desde cero de la vertiente cursiva para los 5 pesos (Light Italic, Regular Italic, Medium Italic, Semibold Italic, Bold Italic).
- Compilación e incorporación de formatos web (`.woff` / `.woff2`).
- Incorporación de Small Caps (versalitas) y figuras numéricas adicionales.

### [v2.0.0] - Fecha TBD
**Enfoque:** Variable Font (VF)
- Compilación de la versión variable (`LEDSText-VF.ttf`) con ejes de peso (`wght`: 300-700) e inclinación (`ital`: 0-1).
