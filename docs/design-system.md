# Design System

---

## Paleta de colores

| Rol | Nombre | Hex |
|-----|--------|-----|
| Primary | Púrpura Aave | #7C3AED |
| Primary light | Púrpura claro | #A78BFA |
| Background | Negro profundo | #0D1117 |
| Surface | Card oscura | #161B22 |
| Surface 2 | Input fondo | #1C2333 |
| Border | Borde sutil | #30363D |
| Text primary | Blanco suave | #E6EDF3 |
| Text secondary | Gris claro | #8B949E |
| Success | Verde seguro | #10B981 |
| Warning | Naranja atención | #F59E0B |
| Error | Rojo peligro | #EF4444 |

---

## Tipografía

- **Display / Headings:** Inter, sans-serif (Google Fonts)
- **Body / Labels:** Inter, sans-serif
- **Números / Monospace:** JetBrains Mono, monospace

| Nivel | Tamaño | Peso |
|-------|--------|------|
| H1 | 28px | 700 |
| H2 (card title) | 18px | 600 |
| Label | 13px | 500 |
| Value destacado | 32px | 700 |
| Body | 15px | 400 |
| Caption | 12px | 400 |

---

## Espaciado y grid

- Escala: 4px base (4, 8, 12, 16, 24, 32, 48)
- Layout: columna centrada, max-width 900px
- Grid de resultados: 2 columnas en desktop, 1 en móvil
- Gutter entre cards: 16px

---

## Estilo de componentes

- Border radius: 12px para cards, 8px para inputs y botones, 6px para badges
- Sombras: sutil en cards (`0 1px 3px rgba(0,0,0,0.4)`)
- Inputs: fondo `#1C2333`, borde `#30363D`, focus con borde púrpura
- Indicador de riesgo: barra de progreso de color semántico (verde → naranja → rojo)
- Iconos: SVG inline, tamaño 18-20px

---

## Tono visual

Profesional y técnico, estética DeFi/crypto. Oscuro porque los usuarios de DeFi prefieren dark mode.
La información numérica es el protagonista — tipografía monospace para valores, colores semánticos para riesgo.
Sin decoraciones gratuitas. Nada de gradientes llamativos. Densidad media: suficiente espacio para respirar.

---

## Componentes definidos

### RiskBadge
Muestra el nivel de riesgo con color semántico.
Estados: `safe` (verde, HF > 1.5), `warning` (naranja, HF 1.1–1.5), `danger` (rojo, HF < 1.1)

### MetricCard
Card con label superior, valor destacado y descripción inferior.
Usada para: precio de liquidación, HF, LTV, caída%.

### ProgressBar
Barra horizontal que muestra el HF relativo a 1 (liquidación).
Color cambia según nivel de riesgo.

### InputGroup
Label + input numérico + sufijo (%, USD, etc.).
Validación inline con borde rojo si el valor es inválido.
