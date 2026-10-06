# Seguridad de retiros

Los retiros mueven fondos a una dirección externa, por lo que cada retiro requiere **verificación reforzada**. Actualmente solo se admite **Authenticator (TOTP)**.

![Verificación reforzada de retiro](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Método de verificación

- **El único método: un código de Authenticator** (Google / Microsoft Authenticator, 1Password, etc.)
- Si no hay ningún Authenticator vinculado, el flujo de retiro te pedirá que actives uno primero en Ajustes
- **Las Passkeys y los códigos por email no se pueden usar para retiros** (siguen funcionando para el inicio de sesión, etc.)

Puedes encontrar la descripción de "Withdrawal step-up verification" (verificación reforzada de retiro) en Ajustes.

***

## Qué hacer al retirar

1. Asegúrate de tener un Authenticator vinculado
2. Rellena la dirección de Polygon y el importe en la página de retiro y compruébalos de nuevo
3. En el diálogo de verificación reforzada, introduce el código de 6 dígitos
4. Envía el retiro una vez superada la verificación

Si el código es incorrecto o ha caducado, simplemente vuelve a introducir el código actual.

***

## Protección adicional

| Mecanismo | Descripción |
|-----------|-------------|
| Máximo retirable | Los fondos inmovilizados en posiciones y órdenes no se pueden retirar |
| Periodo de espera por dispositivo nuevo / red nueva | Es posible que los retiros no estén disponibles temporalmente tras cambiar de dispositivo o de IP |
| Canal de retiro ocupado | En horas punta puede que tengas que esperar de minutos a horas; tus fondos están seguros |
| La billetera de destino necesita MATIC | Mantén un poco de MATIC (POL) en la nueva dirección, o después no podrás mover este USDC on-chain |
| Restricciones de trading | Si el trading de la cuenta está restringido, los retiros también pueden verse afectados |
| Comprobación de la dirección | Los fondos enviados a una dirección externa equivocada normalmente no se pueden recuperar |

***

## Consejos de seguridad

- Nunca des tu código de Authenticator a nadie que diga ser de soporte
- Nunca cambies la dirección de retiro por una "dirección intermedia" que te dé otra persona
- Para orientación sobre el dominio de email oficial, consulta [Antiphishing](anti-phishing.md)
- Antes de un retiro grande: prueba con un importe pequeño → confirma que llega → luego retira más
