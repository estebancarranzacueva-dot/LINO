# Calculadora de Liquidación — Aave

Calcula el precio exacto al que tu posición de préstamo en Aave sería liquidada.

---

## Qué es esto

Herramienta web client-side para usuarios del protocolo DeFi Aave. Introduce los parámetros de tu posición y obtén en tiempo real:

- **Precio de liquidación** — a qué precio de mercado serías liquidado
- **Factor de salud (HF)** — qué tan lejos estás de la liquidación
- **LTV actual** — tu ratio deuda/colateral vs los límites del protocolo
- **Simulación de liquidación parcial** — cuánto colateral perderías si te liquidan

No requiere conexión a wallet ni a ninguna API. Funciona offline.

---

## Requisitos previos

Solo un navegador moderno. Sin instalación.

---

## Uso

Abre `index.html` directamente en tu navegador, o despliégalo en cualquier hosting estático (GitHub Pages, Netlify, Vercel).

### Parámetros de entrada

| Campo | Descripción | Ejemplo (ETH) |
|-------|-------------|---------------|
| Precio actual del colateral | Precio de mercado del activo colateral | $3,500 |
| Valor del colateral | Total depositado en Aave (USD) | $10,000 |
| Valor de la deuda | Total prestado incluyendo intereses (USD) | $5,000 |
| Liquidation Threshold | Umbral de liquidación del activo | 82.5% |
| LTV máximo | Loan-to-Value máximo del activo | 80% |
| Penalización por liquidación | Bonus del liquidador sobre el colateral | 5% |

### Valores de referencia (Aave v3, Ethereum Mainnet)

| Activo | LT | LTV máx | Penalización |
|--------|----|---------|--------------|
| ETH / wstETH | 82.5% | 80% | 5% |
| WBTC | 75% | 70% | 10% |
| LINK | 67% | 65% | 10% |
| USDC / DAI | 78% | 75% | 5% |

Verifica siempre los valores actuales en [app.aave.com](https://app.aave.com).

---

## Fórmula principal

```
Precio_liquidación = (Deuda_USD × Precio_actual) / (Colateral_USD × Liquidation_Threshold)
Factor_salud       = (Colateral_USD × Liquidation_Threshold) / Deuda_USD
```

---

## Cómo contribuir o trabajar en el proyecto

1. Lee `CLAUDE.md` antes de hacer cualquier cambio.
2. Consulta `docs/` para entender las decisiones de diseño y arquitectura.
3. Registra cualquier cambio relevante en `changelog/`.
4. Si tienes ideas de mejora que no entran ahora, añádelas a `mejoras/`.

---

## Estado del proyecto

En desarrollo · Última actualización: 2026-05-11
