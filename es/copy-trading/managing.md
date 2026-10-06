# Gestionar copias

Gestiona todas tus reglas de copia en **My copies** (mis copias) → `/copy-rules`.

![Mis copias](../.gitbook/assets/my_copies_doc.png)

***

## Resumen en la parte superior de la página (habitual)

| Campo | Significado |
|-------|---------|
| Realized | P&L realizado de las posiciones cerradas |
| Position | Resumen del valor de mercado de las posiciones actuales |
| Unrealized | P&L flotante |
| Win Rate | Estadísticas de ganadas / perdidas |

Si aún no has creado ninguna regla, la página puede mostrar una guía de introducción: Iniciar sesión → Depositar → Comprar Gas → Empezar a copiar.

***

## Estados de la regla

| Estado | Significado | Qué hacer |
|--------|---------|------------|
| **Following** | Copiando con normalidad | Solo vigila el historial de operaciones |
| **Manually paused** | La pausaste tú mismo | Reanúdala cuando lo necesites |
| **Funding alert** | Las compras se ven afectadas por problemas de fondos / Gas | Deposita o compra Gas y luego toca **Resume buys** (reanudar compras) |

> Cuando los fondos escasean, las reglas **suelen seguir activas** y solo se omiten las compras: es así por diseño, para que después de recargar puedas seguir copiando las ventas de las posiciones existentes.

***

## Acciones sobre una regla

| Acción | Descripción |
|--------|-------------|
| Pause / Resume | Pausar o reanudar toda la regla |
| Resume buys | Eliminar la alerta de fondos y seguir copiando compras |
| Edit | Cambiar el importe, el porcentaje, el slippage, etc. |
| Delete | Eliminar la regla (el historial normalmente se conserva) |
| Positions / Activity / Detail | Ir a las posiciones, la actividad o el perfil |

También se admite pausar / reanudar / eliminar en bloque (consulta la interfaz).

***

## Pausar vs. Eliminar

| | Pausar | Eliminar |
|--|-------|--------|
| ¿Se puede restaurar rápidamente después? | Sí, con Resume | Hay que crear la regla de nuevo |
| Historial de operaciones | Se conserva | Normalmente se conserva |
| Posiciones existentes | **No** se venden automáticamente | **No** se venden automáticamente |

Cierra las posiciones tú mismo en **Positions**, o espera a la liquidación y canjéalas.

***

## Páginas relacionadas

| Página | Ruta | Propósito |
|------|------|---------|
| Actividad de copia | `/feed` | Ver las ejecuciones públicas de los líderes y las etiquetas de estado de copia |
| Historial de operaciones | `/executions/records` | Los resultados de tus ejecuciones |
| Posiciones | `/executions/positions` | Posiciones y cierre |
| P&L diario | `/executions/daily-pnl` | P&L realizado diario |

![Actividad de copia](../.gitbook/assets/feed_doc.png)

Las etiquetas de estado de Copy activity te ayudan a entender "si se intentó copiar esta ejecución pública"; **el historial de operaciones tiene la última palabra**.

***

## Más información

- Por qué cada operación se copió o no: [Actividad de copia](copy-activity.md)
- Posiciones y liquidación: [Mis posiciones e historial de operaciones](positions-and-records.md)
- Pruébalo sin gastar dinero real: [Copy trading simulado](simulation.md)
