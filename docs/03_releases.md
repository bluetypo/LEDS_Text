# Registro de Releases — LEDS Text

Este archivo documenta la hoja de ruta (*roadmap*), lanzamientos de producción e hitos técnicos en la vida del proyecto tipográfico **LEDS Text**.

---

## [v1.3.0] - 2026-08-29 (Actual)
**Estado:** Estable / Compilación de Producción  
**Estilos:** 10 estilos (Light, Light Italic, Regular, Regular Italic, Medium, Medium Italic, Semibold, Semibold Italic, Bold, Bold Italic).  
**Enfoque:** Incorporación completa de la vertiente itálica (5 cursivas) en formatos OTF y WOFF, configuración de transformaciones tipográficas (inclinación de 10° y sustitución de formas cursivas `/a`, `/f`, `/g`), vinculación de estilos (*Style Linking*) y actualización de metadatos de versión a 1.300.

### Hitos Técnicos:
- Expansión de la familia de 5 a 10 estilos estáticos.
- Compilación y exportación de 5 estilos itálicos en `builds/otf/proof/` y `builds/woff/proof/`.
- Configuración de filtros de transformación de inclinación (`Slant: 10°`) y variantes cursivas (`a.001`, `f.001`, `g.001`).
- Vinculación completa de 4 estilos (*RIBBI*) y pares itálicos adicionales.
- Sincronización general de binarios OTF y WOFF para toda la familia.

---

## [v1.2.0] - 2026-08-29
**Estado:** Lanzamiento Previo  
**Estilos:** Light, Regular, Medium, Semibold, Bold (5 pesos en versión Upright).  
**Enfoque:** Optimización de trazos y nodos (limpieza de nodos duplicados y segmentos superpuestos), compilación de fuentes Web (WOFF), recompilación OTF y empaquetado de release oficial `LEDS_Text_v1.20.zip` en `builds/release/`.

### Hitos Técnicos:
- Limpieza de nodos duplicados y segmentos superpuestos en el set de 380 glifos.
- Recompilación y actualización de binarios OTF en `builds/otf/proof/`.
- Compilación de binarios Web (WOFF) para los 5 pesos en `builds/woff/proof/`.
- Generación de paquete de distribución oficial consolidado (OTF + WOFF + Docs) en `builds/release/`.

---

## [v1.1.0] - 2026-03-04
**Estado:** Lanzamiento Previo  
**Estilos:** Light, Regular, Medium, Semibold, Bold (5 pesos en versión Upright).  
**Enfoque:** Lanzamiento consolidado de la familia romana en 5 pesos en formato OTF empaquetados en `builds/release/`.

### Hitos Técnicos:
- Compilación de 5 estilos estáticos en formato OTF (Light, Regular, Medium, Semibold, Bold).
- Sincronización del set de 380 glifos en todos los estilos romanos.
- Corrección y validación de metadatos WWS (Weight, Width, Slope) e inspección con Fontbakery.
- Configuración de la estructura del repositorio de desarrollo y documentación homologada para Git.

---

## Próximos Lanzamientos Planificados (Roadmap)

### [v1.4.0] - Fecha TBD
**Enfoque:** Formatos Web Adicionales (WOFF2) y Expansión de Set Tipográfico
- Compilación e incorporación de formatos web de compresión avanzada `.woff2`.
- Integración y ajuste de Small Caps (versalitas) y figuras numéricas adicionales.

### [v2.0.0] - Fecha TBD
**Enfoque:** Variable Font (VF)
- Compilación de la versión variable (`LEDSText-VF.ttf`) con ejes de peso (`wght`: 300-700) e inclinación (`ital`: 0-1).
