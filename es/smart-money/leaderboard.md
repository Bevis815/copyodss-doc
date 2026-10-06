# Clasificación de Smart Money (filtrar por perfil del trader)

La clasificación de Smart Money te ayuda a encontrar traders de Polymarket que vale la pena copiar. Acceso: **Smart money** → `/smart-money` (la página de inicio de la App es ahora la [Clasificación diaria de ganancias del copy pool](copy-pool-board.md); abre Smart money desde el menú).

![Clasificación de Smart Money](../.gitbook/assets/smarket_doc.png)

***

## Qué puedes hacer aquí

1. **Explorar la clasificación** — Ver el P&L, la puntuación, la tasa de acierto, los últimos 7 días y más, en tarjetas o en tabla
2. **Buscar direcciones** — Buscar un trader por la dirección de su billetera
3. **Filtrar** — Categorías, preajustes rápidos y filtros avanzados (nivel, estilo, rangos de métricas, copiabilidad, etc.)
4. **Periodo de clasificación** — General / Semanal / Mensual (el valor por defecto suele ser la clasificación general, que no se ordena simplemente por la puntuación global)
5. **Copiar** — Toca **Follow** (seguir) para abrir los ajustes de copia, o abre primero el perfil y decide allí

***

## Cómo se calculan los datos de la clasificación (lectura obligatoria)

- Las curvas de P&L, la ganancia de los últimos 7 días / total, etc. suelen proceder de los datos oficiales de PnL de Polymarket
- La tasa de acierto, el factor de beneficio, etc. se basan principalmente en **mercados cerrados**
- Las puntuaciones y las métricas de backtest se basan en **ejecuciones de una ventana reciente** (unos 30 días / hasta unas 4,000 operaciones), **no en el historial completo**
- La **clasificación mostrada** normalmente solo incluye direcciones cuya puntuación global alcanza un umbral (p. ej., ≥ 40); las direcciones que obtienen puntuaciones bajas repetidamente pueden salir de ella
- "Copy fit / backtest P&L / slippage" y similares son principalmente **simulaciones que asumen retraso + slippage**, no el P&L real de los usuarios que copian en la plataforma

> La clasificación **no es asesoramiento de inversión**. El rendimiento pasado no garantiza rentabilidades futuras.

***

## Filtros habituales

### Ejemplos de categorías

Todas, Política, Deportes, Esports, Cripto, Cultura, Clima, Economía, Tecnología, Finanzas, Menciones y más.

### Ejemplos de filtros rápidos

| Preajuste | Propósito aproximado |
|--------|---------------|
| Featured | Traders destacados por la plataforma, con tendencia a ser copiables |
| Steady | Estilo relativamente conservador |
| High copyability | Más fáciles de seguir en la simulación |
| Recently active | Operaciones más frecuentes en la ventana reciente |
| All copyable | Direcciones disponibles para copiar |
| High win rate / High return / Low drawdown | Acotar según la métrica correspondiente |
| Long-term stable | Candidatos con mejor constancia |

### Filtros avanzados (opciones habituales)

- Solo direcciones copiables / Solo destacados (excluyendo market makers)
- Nivel (S–D), estilo de trading
- Rangos de métricas (p. ej., operaciones en los últimos 7 días, tasa de acierto)
- Excluir etiquetas de riesgo específicas
- Copiabilidad: Alta / Media / Baja

***

## Etiquetas de estilo de trading (como referencia)

| Etiqueta | Significado (simplificado) |
|-----|----------------------|
| Ventaja informativa | Tiende a posicionarse pronto / guiado por la información |
| Arbitraje | Patrones de spread / arbitraje |
| Apostador | Patrones de apuesta de alta volatilidad; cópialo con especial precaución |
| Market maker | Creación de mercado de alta frecuencia; normalmente no es adecuado para la copia habitual |
| Mixto | Estilo mixto general |

***

## Sugerencias

1. Empieza con preajustes como Featured / High copyability / Steady para acotar el campo
2. Abre el perfil para revisar los factores de la puntuación, el drawdown y las notas de riesgo
3. Síguelo con un importe pequeño para probar y luego ajusta gradualmente
4. Al compartir un trader, usa el formato de enlace del perfil: `https://app.copyodds.io/@0xADDRESS` (añade `/zh` para la interfaz en chino)

***

## Páginas relacionadas

- **Leaderboard** de la página de inicio (ganancia diaria del copy pool): [Clasificación diaria de ganancias del copy pool](copy-pool-board.md)
- Cómo plantearse la elección de traders: [Cómo elegir un trader](how-to-choose.md)
