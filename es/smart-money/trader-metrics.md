# Entender las métricas del trader

Las cifras de la clasificación y de las páginas de perfil no siempre se calculan de la misma manera. A continuación se muestran los campos que verás con más frecuencia. **Todas las métricas son solo de referencia y no garantizan el rendimiento futuro.**

***

## Puntuación global y nivel

| Concepto | Descripción |
|---------|-------------|
| **Overall score / Trader score** | Resultado de un modelo multifactorial; cuanto más alta, normalmente mejor es el rendimiento global |
| **Puesto en la clasificación** | La clasificación general por defecto puede combinar varias clasificaciones y **no** se ordena simplemente por la puntuación global |
| **Nivel (S–D)** | Una etiqueta de nivel de calidad para la dirección (p. ej., S = smart money de primer nivel → D = precaución / alto riesgo) |
| **Riesgo** | Indicaciones del nivel de riesgo, como Bajo / Medio / Alto |

### Factores de la puntuación (habituales)

| Factor | Significado (simplificado) |
|--------|----------------------|
| Ventaja | Ventaja en la predicción / fijación de precios |
| Rentabilidad | Capacidad de ganar dinero |
| Copiabilidad | Si es fácil seguirlo con los supuestos de retraso y slippage |
| Salud del drawdown | Si los drawdowns están bajo control |
| Constancia | Si el rendimiento es sostenido y estable |
| Penalización por estilo | Rasgos como la concentración en apuestas pueden reducir la puntuación |

La ventana de puntuación es principalmente una muestra reciente, no todo el historial de la cuenta desde su creación.

***

## Métricas habituales de listas / tarjetas

| Métrica | Cómo interpretarla |
|--------|----------------|
| **P&L total** | P&L según la metodología indicada; fíjate en si es una ventana reciente o el servicio oficial de PnL |
| **P&L de 7 días** | Rendimiento a corto plazo; tiene menos sentido cuando es volátil |
| **Tasa de acierto** | Proporción de muestras cerradas acertadas; una tasa de acierto alta ≠ ganancia garantizada |
| **Drawdown / DD** | Caída desde el máximo; cuanto más bajo, normalmente mejor |
| **Copy fit** | Copiabilidad simulada: Alta / Media / Baja |
| **Factor de beneficio** | Métrica de tipo ratio entre las ganancias totales y las pérdidas totales |
| **Estabilidad / Actividad** | Relacionadas con la volatilidad de la rentabilidad y la frecuencia de operaciones |
| **Operaciones de 7 días / Volumen** | Si sigue operando activamente |
| **Rentabilidad media cerrada** | Métrica de tipo rentabilidad media de las muestras cerradas |

Las columnas marcadas como "simuladas" (backtest P&L, pérdida de copia, slippage, etc.) son simulaciones **que asumen ejecuciones con retraso**, **no** resultados reales de copia de los usuarios de la plataforma.

***

## Resumen del perfil (campos habituales)

| Campo | Descripción |
|-------|-------------|
| Fondos actuales | Referencia del tamaño del capital del trader |
| P&L total / P&L no realizado | P&L realizado y P&L flotante de las posiciones abiertas |
| Volumen total | Referencia de la actividad de trading |
| Rentabilidad total / Margen de beneficio medio | Ratios de tipo rentabilidad |
| Ganadas / Perdidas | Estructura de la muestra |
| Factor de beneficio | Calidad de las ganancias |
| Mayor ganancia / Mayor pérdida (drawdown) | Riesgo de cola |
| Actividad reciente | Si sigue operando |

***

## "Rendimiento real de copia" vs. "Simulación de copia"

| Tipo | Significado |
|------|---------|
| **Simulación de copia** | El sistema hace un backtest de "qué pasaría si copiaras" con supuestos de retraso + slippage |
| **Rendimiento real de copia** | Muestras de usuarios que realmente copian esta dirección en la plataforma (ROI, P&L de copia, suscriptores, etc.); puede ocultarse cuando las muestras son insuficientes |

**Ninguno de los dos** garantiza tus resultados después de copiar.

***

## Consejos de lectura

1. Mira la puntuación, el drawdown y la copiabilidad antes que el P&L total
2. Con muy pocas muestras, la tasa de acierto y el ROI se distorsionan fácilmente
3. En direcciones de market makers / con apuestas extremadamente concentradas, unas métricas atractivas no significan que sean adecuadas para copiar
4. En última instancia, juzga los resultados de la copia por tu propio **Trade history** (historial de operaciones)
