# Ajustes de copia

Qué significa cada parámetro del asistente de copia. Para los campos que no aparecen en el asistente (como algunos límites diarios o retrasos), guíate por la interfaz actual de la App; es posible que los límites avanzados de documentación anterior se hayan consolidado.

***

## Ajustes básicos

| Ajuste | Descripción |
|---------|-------------|
| **Leader address** | La dirección de la billetera que se va a copiar; debe ser correcta |
| **Name** | Nombre visible de la regla, opcional |
| **Copy mode** | Elige uno: **Ratio** (por defecto) / **By balance %** / **Fixed amount** |
| **Copy ratio** | Solo en modo Ratio: ejecución del líder × ratio = el importe de tu orden |
| **Slippage tolerance** | Desviación aceptable respecto al precio de ejecución del trader; por defecto **15%**, ajustable de 1% a 100% |

### Cómo plantearse el slippage

Slippage **demasiado ajustado**: es más probable que se omita o falle cuando los precios se mueven.  
Slippage **demasiado holgado**: es más probable que se ejecute, pero posiblemente a un precio peor.  
El valor por defecto del 15% busca mejorar la tasa de ejecución; ajústalo a tu propio apetito de riesgo. El modo Ratio también tiene dos parámetros adicionales, "Leader order size range" y "Copy ratio": consulta [Los tres modos de copia](copy-modes.md).

***

## Parámetros del modo Ratio

| Ajuste | Descripción |
|---------|-------------|
| **Copy ratio** | 0.1%–100%; la página muestra un valor sugerido junto a "unas N operaciones/día" |
| **Leader order size range** | Se deriva de la mayor ejecución histórica del líder; por debajo del límite inferior se omite, por encima del límite superior se calcula como "límite superior × ratio" |

Para la explicación completa y ejemplos, consulta [Los tres modos de copia](copy-modes.md).

***

## Ajustes avanzados

| Ajuste | Descripción |
|---------|-------------|
| **Direction · Both sides** | Copiar tanto compras como ventas |
| **Direction · Buy only** | Copiar solo compras |
| **Direction · Sell only** | Copiar solo ventas |
| **Max open copy buys** | Número máximo de compras de copia simultáneas bajo la misma regla; **por defecto 1 = sin aumentar posiciones**; el máximo se muestra como **All = ilimitado** |

### ¿Por qué no se aumentan posiciones por defecto?

Las posiciones en un mismo mercado de predicción pueden acumularse rápidamente. El valor por defecto de 1 ayuda a limitar el riesgo en un solo mercado; súbelo cuando hayas confirmado que la estrategia te conviene.

***

## Comportamiento por defecto de la plataforma (conviene saberlo)

- **Retraso de copia**: actualmente el producto normalmente lo intenta de inmediato (sin retraso artificial adicional)
- **Pausa tras fallos consecutivos**: la plataforma puede pausar brevemente las compras tras fallos repetidos (los umbrales exactos pueden variar); tras solucionar el problema, puedes reanudar en **My copies** (mis copias)

***

## "Límites flexibles" relacionados con los fondos

No son necesariamente ajustes, pero actúan como límites:

| Situación | Efecto |
|-----------|--------|
| Gas = 0 | Las compras se omiten; compra Gas y toca **Resume buys** (reanudar compras) |
| USDC insuficiente | Las compras se omiten; deposita más o reduce el importe / porcentaje |
| Por debajo de unos $1 | Es posible que las compras no alcancen el nocional mínimo del exchange |

***

## Cambiar los ajustes

1. Abre **My copies**
2. Busca la regla → **Edit** (editar)
3. Después de guardar, solo se ven afectadas las ejecuciones futuras

Si la simulación está habilitada en tu entorno, puede mostrar más parámetros de tipo límite; para la copia real, lo que cuenta son los campos del asistente.

***

## Campos de la página Quick copy

Además de empezar una copia desde el perfil de un trader, también puedes pegar una dirección directamente en la página **Quick copy** (copia rápida) (`/copier`):

| Campo | Descripción |
|-------|-------------|
| **Copy ratio** | Sigue con un porcentaje de tu saldo disponible; 100% usa el saldo completo, 5% es una posición ligera |
| **Per-trade cap (USDC)** | Lo máximo que pondrás en una sola operación |
| **Total cap (USDC)** | Lo máximo que pondrás en todas las copias combinadas |
| **Auto-copy toggle** | Cuando está activado, el sistema usa tu billetera custodiada para copiar automáticamente las órdenes de este usuario |

Configurar de nuevo la misma dirección **sobrescribe** la regla anterior; después de hacer cambios, compruébalo una vez en **My copies**.
