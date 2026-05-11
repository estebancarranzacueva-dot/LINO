# Calculadora de liquidación Aave — implementación inicial

**Fecha:** 2026-05-11 19:30
**Tipo:** Feature

## Qué se hizo

Implementación completa de la calculadora de precio de liquidación para el protocolo Aave.

Funcionalidades incluidas:
- Cálculo de precio de liquidación en tiempo real
- Factor de salud con barra visual de progreso
- LTV actual vs LTV máximo y Liquidation Threshold con barra comparativa
- Indicador de riesgo semántico (seguro / atención / peligro)
- Simulación de liquidación parcial al 50% (comportamiento real de Aave)
- Tooltips explicativos en cada campo
- Diseño responsive dark mode
- Funciona 100% offline, sin dependencias externas (excepto Google Fonts)

## Qué se modificó

- `index.html` — creado desde cero (HTML + CSS + JS vanilla, archivo único)
- `README.md` — actualizado con descripción, uso y tabla de parámetros de referencia
- `docs/prd.md` — completado con requisitos del producto
- `docs/architecture.md` — completado con stack, fórmulas y decisiones técnicas
- `docs/design-system.md` — completado con paleta, tipografía y componentes

## Por qué

El repositorio estaba inicializado con plantillas vacías. El usuario necesitaba una herramienta práctica para gestionar el riesgo de liquidación en Aave sin depender de backends ni APIs externas.
