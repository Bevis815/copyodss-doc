# Historial de transacciones

**Transaction history** (historial de transacciones) registra cada movimiento de fondos que entra y sale de tu cuenta, además del gasto de Gas: piensa en él como un extracto bancario.

Acceso: **Transaction history** → `/wallets/ledger` (normalmente accesible desde las páginas de depósito / retiro)

***

## Campos de la tabla

| Campo | Significado |
|-------|---------|
| **Network / Asset** | p. ej., Polygon (PoS) + USDC, BSC + USDT, Platform + Gas |
| **Type (In / Out)** | Entrada o salida |
| **Status** | Received, Completed, Posted (recibido, completado, registrado) |
| **Balance after** | Cuánto queda en la cuenta después de esta entrada |
| **View on-chain** | Abrir esta transacción en un explorador de bloques |

Tres tipos de registros:

| Tipo | Descripción |
|------|-------------|
| **Depósito** | USDC / USDT transferido desde una billetera externa |
| **Retiro** | Enviado a tu propia dirección |
| **Gasto de Gas** | Créditos de comisión de servicio descontados por cada ejecución de copia |

***

## Cuando las cifras no cuadran

| Síntoma | Qué comprobar |
|---------|---------------|
| El depósito no aparece | ¿La red era la correcta, el activo es USDC/USDT, la dirección coincide exactamente con la de la página para esa red, está confirmado on-chain (BSC es más lenta)? |
| Retiro atascado en "Processing" | Primero debes completar la verificación reforzada de retiro; puede haber un periodo de espera tras un dispositivo nuevo o un cambio relacionado con el riesgo |
| Se descontó más Gas del esperado | Cada compra y cada venta se cobra con aproximadamente un 0.5% del importe ejecutado; compáralo con el ejemplo de [Gas de la plataforma](gas.md) |
| El saldo no coincide con las posiciones | Las posiciones y las órdenes abiertas inmovilizan fondos; guíate por **Max withdrawable** |

Si no lo encuentras, envía a soporte la **hora, el importe y el estado** del registro junto con el hash on-chain.
