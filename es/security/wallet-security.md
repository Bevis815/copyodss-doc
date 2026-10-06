# Seguridad de la billetera

CopyOdds usa un modelo de **cuenta de trading custodiada**: no necesitas proteger tú mismo las claves privadas de trading, pero sí debes proteger tus métodos de inicio de sesión y la verificación de retiros.

Descripción completa en la App: **Asset security guarantee** (garantía de seguridad de los activos) → `/wallets/security`.

![Garantía de seguridad de los activos](../.gitbook/assets/wallet_security_doc.png)

***

## Mecanismos principales

| Capacidad | Descripción |
|------------|-------------|
| **Billetera dedicada** | Cada usuario tiene una billetera custodiada independiente; los activos se gestionan de forma aislada |
| **Aislamiento de claves privadas** | Las claves privadas de las billeteras se cifran y aíslan por separado, y nunca se exponen directamente a la interfaz de trading diaria |
| **Protección de retiros** | Los retiros requieren verificación reforzada; los cambios en ajustes de seguridad clave pueden activar una nueva verificación / un periodo de espera |

***

## Garantía de seguridad de la plataforma (resumen)

Si los activos de los usuarios se pierden como consecuencia directa de un incidente de seguridad de la **propia plataforma** CopyOdds, como una vulnerabilidad de seguridad o una intrusión en los servidores, la plataforma ofrecerá una compensación de acuerdo con su política de garantía de seguridad (sujeta a la página del producto y a los términos legales).

Ten en cuenta:

- La plataforma **nunca** te pedirá tu frase semilla, clave privada, contraseña ni códigos de verificación por mensaje directo, email o soporte
- Las pérdidas de trading en mercados de predicción, los errores del usuario (cadena equivocada, dirección equivocada), las estafas de phishing, etc. no están cubiertos por la "compensación por incidentes de seguridad de la plataforma"
- Usa siempre el dominio oficial

***

## Lo que debes hacer tú mismo

1. Usa solo el sitio web / la App oficial: **copyodds.io**
2. **Activa Authenticator** (obligatorio para los retiros; consulta [Autenticación de dos factores (2FA)](2fa.md))
3. Opcionalmente, añade una Passkey para iniciar sesión más fácilmente
4. Revisa periódicamente tus [dispositivos con sesión iniciada](../account/devices-and-passkeys.md) y elimina los que no reconozcas
5. Deposita usando la dirección de la página y compruébala con **Verify deposit address** (verificar dirección de depósito)
6. Prueba tu primer depósito y tu primer retiro con importes pequeños

***

## Páginas relacionadas

- Depósito / Retiro: `/wallets/deposit`, `/wallets/withdraw`
- Ajustes de seguridad: `/settings`
- Gestión de dispositivos: `/settings/devices`
- Passkeys: `/settings/passkeys`

***

## ¿Quieres comprobarlo tú mismo?

- Movimientos de fondos y gasto de Gas: **Transaction history** → `/wallets/ledger` (consulta [Historial de transacciones](../wallet/ledger.md))
- Dispositivos en los que has iniciado sesión y periodos de espera para retiros: **Settings → Devices** → `/settings/devices` (consulta [Dispositivos y Passkeys](../account/devices-and-passkeys.md))
