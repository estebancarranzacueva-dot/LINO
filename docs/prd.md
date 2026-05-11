# Product Requirements Document (PRD)

---

## Resumen ejecutivo

Calculadora web para usuarios del protocolo DeFi Aave que permite calcular el precio exacto al que una posición de préstamo sería liquidada. El usuario introduce los parámetros de su posición (colateral, deuda, umbrales) y obtiene en tiempo real el precio de liquidación, el factor de salud y métricas de riesgo clave.

---

## Problema que resuelve

Los usuarios de Aave que abren posiciones de préstamo con colateral necesitan saber con precisión a qué precio de mercado su colateral sería liquidado. Sin esta información, es difícil gestionar el riesgo y decidir cuándo añadir más colateral o devolver deuda. La interfaz de Aave muestra el factor de salud pero no el precio exacto de liquidación de forma prominente.

---

## Usuario objetivo

**Persona principal: Trader DeFi activo**
- Usa Aave para pedir prestado stablecoins contra ETH, BTC u otros activos
- Quiere saber exactamente cuánto puede caer el precio antes de ser liquidado
- Necesita recalcular rápidamente cuando cambia el precio o ajusta su posición
- Nivel técnico: intermedio-avanzado en cripto, no necesariamente en código

---

## Funcionalidades core (MoSCoW)

### MUST
- Calcular precio de liquidación a partir de: precio actual, valor colateral USD, valor deuda USD, liquidation threshold
- Mostrar factor de salud actual
- Mostrar LTV actual vs LTV máximo
- Mostrar caída porcentual necesaria para ser liquidado
- Indicador visual de nivel de riesgo (seguro / atención / peligro)
- Funcionar sin backend (calculadora client-side)

### SHOULD
- Mostrar cantidad de colateral que recibiría el liquidador (con penalización)
- Inputs con validación en tiempo real
- Diseño responsive (móvil y escritorio)

### COULD
- Simulador: "si el precio baja a X, ¿cuál sería mi HF?"
- Soporte para múltiples activos de colateral

### WON'T (esta versión)
- Conexión a wallets o blockchain
- Historial de posiciones
- Datos de precio en tiempo real

---

## Flujos de usuario principales

**Flujo principal:**
El usuario abre la página, introduce los parámetros de su posición en Aave (precio actual del activo, valor del colateral en USD, valor de la deuda en USD, liquidation threshold, LTV máximo y penalización por liquidación), y la calculadora muestra automáticamente el precio de liquidación, el factor de salud, el LTV actual y la caída porcentual necesaria para ser liquidado.

---

## Requisitos no funcionales

- Funciona offline (sin llamadas a APIs externas)
- Tiempo de respuesta de cálculo: instantáneo (< 16ms)
- Compatible con Chrome, Firefox, Safari modernos
- Responsive: funciona en móvil desde 320px de ancho

---

## Fuera de alcance (explícito)

- Autenticación de usuarios
- Base de datos o backend
- Precios en tiempo real
- Soporte multi-colateral en una sola posición
