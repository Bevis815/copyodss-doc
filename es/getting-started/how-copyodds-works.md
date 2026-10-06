# Cómo funciona CopyOdds

Desde "un trader obtiene una ejecución" hasta "tu cuenta intenta copiarla", el flujo completo es así:

```text
Un trader de smart money obtiene una ejecución en Polymarket
        ↓
CopyOdds detecta la ejecución pública
        ↓
La asocia con tu regla de copia para esa dirección
        ↓
Calcula el tamaño de la orden según la regla (importe fijo o % de tu saldo)
        ↓
Intenta colocar la orden dentro del slippage (consume Gas de la plataforma)
        ↓
El resultado se registra en Trade history; las tenencias aparecen en Positions
```

## 1. Descubrir traders

- El sistema puntúa y filtra continuamente las billeteras públicas de Polymarket
- La **clasificación mostrada** normalmente exige que la puntuación global alcance un umbral (p. ej., ≥ 40); las direcciones con puntuación baja pueden salir de ella
- En **Smart money** puedes explorar, buscar o analizar direcciones no listadas (si la función está disponible, puede aplicarse un límite diario)

## 2. Los fondos y las comisiones están separados

| Recurso en la cuenta | Propósito |
|---------------------|---------|
| **USDC (etc.)** | Capital de copia: se usa al comprar y se devuelve al vender |
| **Gas de la plataforma** | Créditos de comisión de servicio: se descuenta aproximadamente un 0.5% del importe nocional por cada ejecución de copia |

Cuando el Gas es 0: **no puedes crear / reanudar reglas de copia**. Las reglas existentes normalmente siguen funcionando, pero **las compras se omiten**; las ventas aún pueden copiarse si tienes posiciones.

## 3. Cómo se aplican las reglas de copia

Guardas una regla por cada dirección líder (volver a guardar para la misma dirección la sobrescribe):

- **Modo de copia** (elige uno; por defecto **Ratio**):
  - **Ratio**: cada ejecución del líder × tu ratio = el importe de tu orden
  - **By balance %**: cada operación usa un porcentaje de tu propio USDC disponible
  - **Fixed amount**: cada operación compra el mismo importe
  - Consulta [Los tres modos de copia](../copy-trading/copy-modes.md)
- **Dirección**: Ambas / Solo compra / Solo venta
- **Slippage**: no hay ejecución si el precio se mueve demasiado (por defecto 15%)
- **Ratio de copia / Rango de tamaño** (solo en modo Ratio): controla "cuánto copiar" y "qué tamaños de orden copiar"
- **Max open copy buys** (máximo de compras de copia abiertas): por defecto 1 (sin aumentar posiciones); se puede aumentar, y el máximo es **All (ilimitado)**

Tras detectar una ejecución del líder, el sistema intenta colocar una orden usando estas reglas. **No garantiza** que se copie cada operación.

## 4. Cómo saber si una operación se copió

| Dónde mirar | Qué te indica |
|---------------|-------------------|
| Copy activity | Lo que hizo el trader |
| Trade history | Los resultados de tus intentos de copia (ejecutado / omitido / fallido) |
| Positions | Lo que tienes actualmente |
| My copies | Estado de la regla: Following / Manually paused / Funding alert |

## 5. Las redes de depósito y de retiro son diferentes (importante)

- **Depósito**: Polygon (PoS) y BSC (cuando está habilitada), activos USDC / USDT
- **Retiro**: solo **USDC en Polygon (PoS)**
- Las dos redes de depósito usan **direcciones diferentes**: nunca las confundas

Consulta [Redes compatibles](../wallet/supported-networks.md).

## 6. El modelo de seguridad en resumen

CopyOdds usa una **cuenta de trading custodiada**: una billetera por usuario, con claves privadas aisladas. Los retiros requieren verificación reforzada con **Authenticator (TOTP)**. Consulta [Seguridad](../security/wallet-security.md).
