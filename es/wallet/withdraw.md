# Retiro

Retira el **USDC** disponible libremente de tu cuenta de trading a una billetera externa. Acceso: **Wallets → Withdraw** → `/wallets/withdraw`.

![Página de retiro](../.gitbook/assets/usdc2_doc.png)

![Verificación reforzada de retiro](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Reglas de retiro

| Elemento | Descripción |
|------|-------------|
| Red | **Solo Polygon (PoS)** |
| Activo | **USDC** |
| Dirección receptora | Debe poder recibir USDC en Polygon; **no** introduzcas la dirección custodiada de la página de depósito, y no puede ser **tu propia dirección de depósito actual** |
| Billetera de destino | Debe tener un poco de **MATIC (POL)**; lo necesitarás para pagar el gas cuando muevas este USDC on-chain más adelante |
| Verificación reforzada | Obligatoria para cada retiro (ver más abajo) |

***

## Pasos

1. Abre la página de retiro y comprueba **Max withdrawable** (máximo retirable) (puede ser inferior a tu saldo total)
2. Introduce una dirección receptora de Polygon y un importe
3. Comprueba de nuevo la red, la dirección y el importe
4. Toca continuar y completa la **verificación reforzada de retiro**
5. Después de enviarlo, sigue el estado en tus extractos / registros

***

## ¿Por qué "Max withdrawable" es menor que mi saldo?

Los siguientes fondos normalmente no se pueden retirar de inmediato:

- Fondos inmovilizados en posiciones abiertas
- Fondos congelados en órdenes no ejecutadas
- Otros márgenes / fondos bloqueados por el sistema

Guíate por la cifra de **Max withdrawable** de la página, no por tu saldo total.

***

## Verificación reforzada de retiro

Cada retiro debe confirmarse con un código de 6 dígitos de **Authenticator (TOTP)**: **actualmente es el único método admitido**.

Si no lo has configurado, el sistema te guiará para activarlo en Ajustes; **no puedes retirar sin él**.

**Las Passkeys y los códigos por email no se pueden usar para confirmar retiros** (solo sirven para el inicio de sesión y escenarios similares).

Consulta [Seguridad de retiros](../security/withdrawal-security.md) y [Autenticación de dos factores (2FA)](../security/2fa.md).

***

## ¿No puedes retirar temporalmente?

| Mensaje | Significado | Qué hacer |
|---------|---------|------------|
| **Withdrawal channel busy** | Muchas solicitudes de retiro hoy | Espera unos minutos u horas según se indique; **tus fondos están seguros y no necesitas volver a enviarlo** |
| **New device / new network cooldown** | Acabas de cambiar de dispositivo o tu IP ha cambiado | Vuelve a intentarlo cuando termine el periodo de espera |
| **Unfilled orders exist** | Todavía tienes órdenes abiertas | Cancélalas o espera a que se ejecuten |
| **Positions still open** | Tu dirección custodiada todavía tiene posiciones en mercados | Ciérralas o espera a la liquidación |
| **Previous withdrawal in progress** | Aún se está confirmando on-chain | Espera a que termine antes de enviar el siguiente |
| **Address is your deposit address** | No puedes retirar de vuelta a tu dirección de depósito | Usa tu propia dirección receptora |

Revisa las sesiones y los ajustes de seguridad en **Settings → Devices / Security**. Si sigue fallando, contacta con soporte e indica si has cambiado de dispositivo recientemente.

***

## Consejos de seguridad

- Antes de tu primer retiro grande: prueba primero con un importe pequeño
- Los retiros normalmente no se pueden deshacer una vez enviados: comprueba la dirección carácter por carácter
- CopyOdds nunca te enviará un mensaje directo para "ayudarte con un retiro" ni te pedirá tus códigos de verificación

***

## Dónde ver los registros de retiro

**Transaction history** (historial de transacciones) → `/wallets/ledger` muestra el estado de cada retiro y el "saldo posterior", con un enlace al explorador de bloques. Consulta [Historial de transacciones](ledger.md).
