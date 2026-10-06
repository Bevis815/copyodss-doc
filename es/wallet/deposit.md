# Depósito

Deposita USDC / USDT en tu **cuenta de trading** de CopyOdds para usarlo como capital de copia. Acceso: **Wallets → Deposit** → `/wallets/deposit`.

![Página de depósito](../.gitbook/assets/usdc1_doc.png)

***

## Deposita en cuatro pasos

1. **Elige la red** — Polygon (PoS) o BSC, la misma red desde la que retiras en tu exchange  
2. **Elige el activo** — Solo **USDC** o **USDT**  
3. **Envía** — Copia o escanea **la dirección que se muestra en esta página**  
4. **Espera** — Tu saldo se actualiza tras la confirmación on-chain; BSC puede tardar unos minutos más

La página también tiene una sección **Deposit steps** (pasos del depósito) con los mismos cuatro pasos, además de un enlace al vídeo **Watch tutorial** (ver tutorial) (`/guide-video`). Te recomendamos verlo antes de tu primer depósito.

### Tres consejos prácticos

| Acción | Descripción |
|--------|-------------|
| **Guarda el código QR** | Toca **Save image** (guardar imagen) para guardar el código QR de la dirección en tu teléfono; escanear es menos propenso a errores que escribir |
| **Copia después de elegir la red** | Después de cambiar a BSC **debes volver a copiar la dirección**: las dos cadenas usan direcciones diferentes |
| **Usa solo la dirección que se muestra actualmente en esta página** | No uses direcciones antiguas del historial de chat ni enviadas por otras personas |

***

## Reglas importantes

| Regla | Descripción |
|------|-------------|
| Redes compatibles | **Polygon (PoS)** (recomendada) y **BSC**; la página muestra etiquetas como "Recommended / Fast / Low fees" |
| La dirección depende de la red | La dirección custodiada de Polygon y la dirección puente de BSC son **diferentes**: nunca las confundas |
| Solo USDC / USDT | Otros tokens normalmente no se pueden acreditar |
| No uses la cadena equivocada | No uses redes no compatibles como Ethereum / Arbitrum |
| Verifica la dirección | Toca **Verify deposit address** (verificar dirección de depósito) y el sistema te enviará la dirección a través del **bot oficial de Telegram** o de tu **email vinculado** para que la compruebes |
| Prefiere USDC | El USDT en Polygon suele aparecer como "USDT (PoS)"; no deposites BNB ni otros tokens |

### Cómo usar Verify deposit address

1. Toca **Verify deposit address**
2. La página te pedirá que inicies el bot oficial de Telegram (`@botname`) o que revises tu email vinculado
3. Cuando recibas la dirección, **compárala carácter por carácter** con la de la página
4. Continúa solo si coincide exactamente

### Tu saldo tiene dos cifras

| Término | Significado |
|------|---------|
| **Saldo on-chain** | El USDC nativo que realmente ha llegado a la blockchain |
| **Saldo negociable** | La parte que la plataforma ha procesado y que se puede usar para copiar |

Si, justo después de un depósito, ves "xx native USDC on-chain, automatically converting to tradable balance", es el flujo normal: espera unos minutos y actualiza.

***

## Detalles

1. Inicia sesión y confirma que tu cuenta de trading está activa
2. En la página de depósito, elige primero la red y luego copia la dirección
3. Al retirar desde tu exchange o billetera: comprueba con cuidado la red, el token y el importe
4. Vuelve a CopyOdds y desliza para actualizar tu saldo si es necesario
5. Antes de tu primer depósito grande: deposita una cantidad pequeña → confirma que llega → luego deposita más

***

## ¿El depósito tarda o no aparece?

Comprueba en este orden:

1. ¿La red de retiro coincide con la seleccionada en esta página (Polygon vs. BSC)?
2. ¿El token es USDC / USDT?
3. ¿La dirección receptora es **exactamente la misma** que la de esta página?
4. ¿La transacción on-chain está confirmada? (Busca el hash en el explorador de bloques correspondiente)
5. ¿Lo enviaste por error a un destino de retiro o a la dirección de otra plataforma?

Si sigue sin aparecer: contacta con soporte indicando el **hash de la transacción, la red, el importe, la hora y el email registrado**.

***

## ¿Qué sigue después de depositar?

- Para empezar a copiar: asegúrate primero de que **Polymarket esté listo** y luego **compra Gas de la plataforma** (consulta [Gas de la plataforma](gas.md))
- Las compras de copia necesitan USDC disponible (se recomienda al menos unos $1)

***

## Dónde comprobarlo cuando llegue

Abre **Transaction history** (historial de transacciones) → `/wallets/ledger` para ver la red, el activo, el estado y el saldo posterior a la transacción del depósito. Consulta [Historial de transacciones](ledger.md).
