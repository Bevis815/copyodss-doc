# Cómo funciona el copy trading

Una vez activada la copia, CopyOdds **intenta** colocar órdenes en tu cuenta de trading según tus reglas cada vez que un trader al que sigues obtiene una ejecución.

**Si una copia tuvo éxito lo determina Trade history** (historial de operaciones); Copy activity (actividad de copia) solo muestra las acciones públicas del trader.

![Historial de operaciones](../.gitbook/assets/change_doc.png)

***

## Flujo de ejecución

1. Detectar la ejecución pública del líder (compra / venta) en Polymarket
2. Buscar tu regla de copia para esa dirección y comprobar que la dirección coincide
3. Calcular el importe nocional objetivo a partir de un **importe fijo** o de un **porcentaje de tu USDC disponible**
4. Intentar colocar la orden dentro de tu tolerancia de slippage
5. Al ejecutarse, descontar el **Gas de la plataforma** correspondiente (aproximadamente un 0.5% del nocional) y actualizar las posiciones / registros

***

## Ejecutada vs. Omitida vs. Fallida

| Resultado | Significado |
|--------|---------|
| **Filled** | La orden de copia se ejecutó |
| **Skipped** | No se colocó ninguna orden debido a los ajustes, los fondos, etc. (habitual) |
| **Failed** | La orden fue rechazada o dio error |
| **Settled, etc.** | Estados de liquidación / completado según muestran los filtros de la interfaz |

### Motivos habituales de omisión

- Discrepancia de dirección (Solo compra / Solo venta)
- Importe por debajo de la compra mínima de aproximadamente **$1**
- Se alcanzó **Max open copy buys** (por defecto 1 = sin aumentar posiciones)
- Slippage demasiado grande
- **Gas insuficiente** o **USDC insuficiente**
- El trader vendió pero tú no tienes la posición correspondiente
- No hay contraparte en el mercado en ese momento

***

## ¿Qué pasa con las reglas cuando los fondos escasean?

| Situación | Estado de la regla | Compras | Ventas (cuando tienes posiciones) |
|-----------|-------------|------|---------------------------------|
| Gas = 0 | Normalmente sigue "en funcionamiento"; puede aparecer una alerta de fondos | Omitidas | Aún pueden copiarse |
| No hay suficiente USDC para comprar | Igual que arriba | Omitidas | Aún pueden copiarse |
| Pausada manualmente | Manually paused | No se copian | No se copian |

Después de recargar Gas / USDC, ve a **My copies** (mis copias) y toca **Resume buys** (reanudar compras) (si toda la regla se pausó manualmente, toca Resume en su lugar).

***

## Copy activity vs. Trade history vs. Positions

| Página | Contenido |
|------|---------|
| Copy activity | Las compras y ventas públicas del trader |
| Trade history | Tus intentos de copia y sus resultados |
| Positions | Tus posiciones actuales; cerrar / canjear acciones liquidadas |
| Daily P&L | Curva de P&L realizado por día de trading |

El P&L realizado de hoy normalmente se reinicia a diario a una hora fija en la zona horaria de tu cuenta (p. ej., a las 8:00 AM); consulta la descripción dentro de la App para más detalles.
