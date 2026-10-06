# Actividad de copia

**Copy activity** (actividad de copia) te indica dos cosas: **lo que el trader acaba de hacer** y **si lo copiaste**.

Acceso: **Copy activity** → `/feed` (normalmente se llega desde **My copies** o desde el menú)

***

## Qué hay en la página

1. **Arriba: billeteras que estoy copiando** — Muestra las direcciones para las que has activado la copia; toca una para ver solo esa
2. **Tres pestañas**

| Pestaña | Contenido |
|-----|---------|
| **Activity** | Las compras / ventas públicas del trader |
| **My orders** | El resultado de cada orden que el sistema colocó por ti |
| **My positions** | Tus posiciones actuales y tu P&L |

3. **Filtros**: All / Successful / Buys / Sells / Copying (todas / con éxito / compras / ventas / copiando)
4. Cada entrada muestra una hora (**just now**, **a few minutes ago**); en el móvil, desliza hacia abajo para actualizar

***

## Interpretar los estados de copia

| Estado | Significado | Qué hacer |
|--------|---------|------------|
| **Copying** | Intentando colocar la orden | Espera un momento |
| **Copied** | Copiada con éxito | Nada |
| **Skipped** | No se copió esta vez | Revisa el motivo del fallo |
| **Failed** | La orden fue rechazada o dio error | Revisa el motivo: posiblemente saldo / slippage / Gas |
| **Not copied** | Esta entrada no está dentro de tu ámbito de copia | Nada |

Toca cualquier entrada para ver los **detalles de la operación**: mercado, dirección, dirección de billetera, volumen, regla de copia, billetera de copia, estado, hora y hash de la transacción on-chain.

***

## Motivos habituales de omisión

- Discrepancia de dirección (configuraste Solo compra / Solo venta)
- Importe demasiado pequeño (por debajo de la compra mínima del exchange de unos $1)
- Se alcanzó "Max open copy buys" (por defecto 1, es decir, sin aumentar posiciones)
- Slippage demasiado grande
- **Gas insuficiente** o **USDC insuficiente**
- El trader vendió pero tú no tienes la posición correspondiente
- Nadie estaba aceptando órdenes en ese mercado en ese momento

***

## Consejos

- Usa **Activity** para observar a otros y **Trade history** (historial de operaciones) para revisarte a ti mismo: comparar ambos es la forma más fácil de detectar problemas
- Si hay muchas omisiones, revisa primero el Gas y el saldo, y luego considera ajustar el slippage o reducir el importe
- Al compartir una entrada con soporte, incluye el **ID del registro** o el **hash de la transacción**
