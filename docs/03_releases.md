# Registro de Releases — LEDS Text

Este archivo documenta la hoja de ruta (*roadmap*), lanzamientos de producción e hitos técnicos en la vida del proyecto tipográfico **LEDS Text**.

---

## [v1.1.0] - 2026-03-04 (Actual)
**Estado:** Estable / Compilación de Producción  
**Estilos:** Light, Regular, Medium, Semibold, Bold (con variantes Upright e Italic, 10 estilos en total).  
**Enfoque:** Lanzamiento completo de la familia con 10 variantes en formato OTF empaquetadas en `builds/otf/release/`.

### Hitos Técnicos:
- Compilación e integración de 10 estilos estáticos en formato OTF (5 pesos en versiones Upright e Italic).
- Sincronización del set de 380 glifos en todos los estilos de la familia (10 fuentes en total).
- Corrección de metadatos WWS (Weight, Width, Slope) e inspección con Fontbakery.
- Asignación correcta de bits de selección (`fsSelection`) para correcta diferenciación de romanas e itálicas en menús de software.
- Configuración de la estructura del repositorio de desarrollo y documentación homologada para Git.

---

## Próximos Lanzamientos Planificados (Roadmap)

### [v1.2.0] - Fecha TBD
**Enfoque:** Versalitas (Small Caps) y Fuentes Web (WOFF / WOFF2)
- Compilación e incorporación de formatos web (`.woff` / `.woff2`) para los 10 estilos.
- Incorporación de Small Caps (versalitas) y figuras numéricas adicionales.
- Expansión de glifos para soporte 100% en Francés y Alemán.

### [v2.0.0] - Fecha TBD
**Enfoque:** Variable Font (VF)
- Compilación de la versión variable (`LEDSText-VF.ttf`) con ejes de peso (`wght`: 300-700) e inclinación (`ital`: 0-1).
