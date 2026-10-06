# Mis posiciones e historial de operaciones

Después de empezar a copiar, todas tus posiciones y el resultado de cada orden están en estas dos páginas. **Como principiante, estas dos páginas son todo lo que necesitas conocer.**

| Página | Acceso | Qué responde |
|------|-------|-----------------|
| **My positions** | My positions → `/executions/positions` | ¿Qué tengo ahora y voy ganando o perdiendo? |
| **Trade history** | Executions → `/executions/records` | El resultado de cada intento de copia |
| **Profit/Loss** | Executions → Profit/Loss → `/executions/daily-pnl` | ¿Cuánto he ganado en este periodo? |

***

## Mis posiciones

### Lo que verás

| Campo | Significado |
|-------|---------|
| **Market / Outcome** | Qué evento y qué resultado (Sí / No) compraste |
| **Avg. price / Current price** | Tu coste de entrada y el precio actual de mercado |
| **Cost / Value / P&L** | Cuánto gastaste, cuánto vale ahora y si vas ganando |
| **Copy sources** | Qué reglas de copia formaron esta posición |
| **Status** | Abierta / Pendiente de liquidación / Liquidada / Archivada |

### Lo que puedes hacer

| Acción | Descripción |
|--------|-------------|
| **Buy more** | Comprar un poco más tú mismo introduciendo un importe en USD |
| **Close** | Vender a mercado para fijar el P&L; el precio se mueve con el mercado |
| **Bulk close** | Cerrar hasta un determinado número de posiciones a la vez |
| **Redeem** | El mercado ha terminado y has ganado: convierte la posición en USDC |
| **View details** | Ver la hora de compra, el método de liquidación y la cronología completa |

### Qué significan los estados

| Estado | Descripción |
|--------|-------------|
| **Open** | El mercado no ha terminado; puedes vender |
| **Pending settlement** | No se puede vender por ahora; si ganaste, aparecerá Redeem; si perdiste, se cierra automáticamente |
| **Settled** | Convertida en USDC y devuelta a tu saldo |
| **Archived** | Posiciones diminutas o sin liquidez que no se pueden vender por ahora; no afecta a nada más |

***

## Historial de operaciones (historial de copias)

Cada fila es un intento que el sistema hizo en tu nombre:

| Estado | Significado |
|--------|---------|
| **Filled** | Copiada con éxito |
| **In progress** | Aún en proceso |
| **Skipped** | No se colocó ninguna orden (consulta el motivo del fallo) |
| **Failed** | La orden fue rechazada o dio error |

Puedes filtrar por **Filled / Settled / Unsuccessful**. Toca cualquier fila para ver: regla de copia, ID de la orden, precio de compra y acciones, cómo se cerró (vendida / canjeada / expirada), coste, ingresos, P&L, cronología completa y hash on-chain.

***

## Página de Profit/Loss

- La parte superior muestra una **curva de P&L acumulado**, que se puede cambiar entre 1 día / 1 semana / 1 mes, etc.
- La parte inferior muestra un **desglose por periodo**, que incluye hoy, ayer y la variación del P&L de la cuenta de cada día
- La curva coincide con la metodología de P&L de cuenta de Polymarket; si los datos oficiales no están disponibles temporalmente, la página indicará que está usando en su lugar los datos del registro de la plataforma

> La hora de inicio del día hábil es la que se muestra en la página (p. ej., a partir de las 08:00), así que tenlo en cuenta al mirar datos de varios días.

***

## Preguntas habituales de principiantes

**¿Por qué el P&L de mis posiciones no coincide con mi saldo?**  
El P&L de las posiciones está "estimado al precio actual de mercado" y la parte no realizada cambia con el precio; tu saldo solo lo refleja cuando vendes o canjeas.

**¿Por qué falló mi venta?**  
Motivos habituales: no había órdenes de compra en el mercado en ese momento, acciones inmovilizadas en órdenes abiertas o la posición restante está por debajo del tamaño mínimo de venta. Inténtalo más tarde.

**He ganado: ¿por qué no veo el dinero?**  
Tarda un poco en acreditarse después de que el mercado se liquide; puedes tocar **Redeem** (canjear) para canjearlo manualmente. Mientras muestre "Pending settlement", todavía no puedes actuar sobre ella.
