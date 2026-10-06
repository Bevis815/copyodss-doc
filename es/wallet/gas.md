# Gas de la plataforma

El **Gas de la plataforma** es un **crédito de comisión de servicio** dentro de tu cuenta de CopyOdds, que se usa para pagar las comisiones de las ejecuciones de copia automatizada.

> **Gas de la plataforma ≠ gas on-chain.** No es MATIC, POL ni BNB, ni el gas que usas en una billetera para pagar las comisiones de red.

Acceso: **Gas Store** → `/store`.

![Gas Store](../.gitbook/assets/store_doc.png)

***

## ¿Por qué necesitas Gas?

Cada ejecución de copia (compra o venta) descuenta créditos de comisión de servicio según el importe nocional de la ejecución. Sin Gas:

- **No puedes crear ni reanudar reglas de copia**
- Con las reglas existentes, **las compras normalmente se omiten**
- Si aún tienes posiciones, **las ventas aún pueden copiarse** (las reglas suelen seguir en funcionamiento)

***

## Comisiones (condiciones actuales del producto)

| Concepto | Descripción |
|------|-------------|
| Comisión | **Tanto las compras como las ventas** cuestan aproximadamente un **0.5%** del importe real ejecutado, descontado en Gas |
| Conversión | Aproximadamente **1 USDC = 100 Gas** |
| Ejemplo | Una ejecución de $100 consume unos **50 Gas** (la compra y la venta se cobran una vez cada una) |
| Origen del pago | Los paquetes se pagan con tu **saldo disponible en USDC** custodiado |
| ¿Se puede retirar? | **No**: no se puede retirar ni transferir |

Consulta la página de la tienda para ver los paquetes actuales y cualquier bonificación (como los incrementos por nivel de referidos).

> Si tienes órdenes sin completar, posiciones abiertas o retiros pendientes, es posible que la tienda temporalmente **no permita comprar Gas con tu saldo** y te pida que lo resuelvas en la página Wallet; una vez resuelto, podrás comprar con normalidad.

***

## Cómo comprar

1. Abre la Gas Store y asegúrate de tener suficiente USDC
2. Lee la descripción de las comisiones
3. Elige un paquete → confirma el pago
4. El Gas se acredita al instante
5. Si antes se omitían compras por falta de Gas: ve a **My copies** (mis copias) y toca **Resume buys** (reanudar compras)

***

## Gas vs. USDC

| | USDC | Gas de la plataforma |
|--|------|--------------|
| Propósito | Capital de copia | Comisión de servicio de copia |
| Cómo obtenerlo | Depósito on-chain | Comprarlo con USDC en la tienda |
| ¿Se puede retirar on-chain? | Sí (consulta Retiro) | No |

***

## Preguntas frecuentes

**¿Tengo que hacer algo después de comprar Gas?**  
Te recomendamos ir a **My copies** y tocar **Resume buys** para eliminar cualquier alerta de fondos.

**¿Se detendrán mis reglas cuando se agote el Gas?**  
Normalmente no se pausa toda la regla: las compras se omiten y las ventas aún pueden copiarse si tienes posiciones.
