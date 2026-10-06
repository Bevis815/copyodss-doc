# Autenticación de dos factores (2FA)

CopyOdds te permite iniciar sesión con un **código de verificación por email** por defecto (sin contraseña tradicional). Te recomendamos activar tanto Authenticator como una Passkey para reforzar la seguridad de los retiros y del inicio de sesión, respectivamente.

![Ajustes de seguridad](../.gitbook/assets/settings_security_doc.png)

***

## Métodos disponibles

| Método | Propósito |
|--------|---------|
| **OTP por email** | Inicio de sesión, verificación de vinculación |
| **Authenticator (TOTP)** | **Verificación reforzada de retiros (el único método)**; también refuerza la seguridad de la cuenta |
| **Passkey** | Rostro / huella dactilar / bloqueo de pantalla para una verificación rápida del **inicio de sesión** |
| **Telegram** | Método opcional de inicio de sesión / vinculación (consulta Ajustes) |
| **Gestión de dispositivos** | Ver y eliminar dispositivos; los dispositivos nuevos pueden afectar a los retiros |

***

## Orden de configuración recomendado

1. Vincula y verifica tu email
2. **Activa Authenticator (obligatorio antes de retirar)**
3. Añade una **Passkey** en los dispositivos que uses a menudo (para iniciar sesión más fácilmente)
4. Familiarízate con la lista de **Devices** (dispositivos) y elimina cualquier dispositivo que no reconozcas

***

## Authenticator (TOTP)

1. Abre **Settings → Security** (ajustes → seguridad)
2. Sigue la guía para escanear el código QR con tu app Authenticator, o introduce la clave manualmente
3. Introduce el código de 6 dígitos para terminar de activarlo

Si llegaste aquí desde el flujo de retiro, al terminar **volverás automáticamente a la página de billetera para continuar con el retiro**.

### Desactivar Authenticator

Por seguridad, **desactivarlo también requiere un código de 6 dígitos**. Si solo quieres cambiar de dispositivo, es más fácil volver a vincularlo en el nuevo dispositivo.

### Mensajes habituales

| Mensaje | Causa | Qué hacer |
|---------|-------|------------|
| El código es incorrecto o ha caducado | Error al escribir, o han pasado más de 30 segundos | Espera a un nuevo código e introdúcelo |
| El código ya se ha usado | Se envió el mismo código dos veces | Espera al siguiente código nuevo |
| La vinculación ha caducado | Pasó demasiado tiempo entre el escaneo y la confirmación | Vuelve a empezar la vinculación |
| Demasiados intentos | Demasiados intentos incorrectos en poco tiempo | Espera un rato y vuelve a intentarlo |
| Authenticator ya activado | Se intenta vincular por segunda vez | No es necesario volver a hacerlo |

***

## Passkey

1. Abre Ajustes en un navegador / sistema operativo compatible
2. Añade una Passkey y completa la verificación biométrica o con bloqueo de pantalla según se indique
3. En la página de inicio de sesión puedes elegir Passkey para iniciar sesión rápidamente

Nota: una Passkey **no** se puede usar para confirmar retiros. La compatibilidad varía según el navegador, el WebView y la versión del sistema operativo; si el inicio de sesión falla, recurre al código por email.

***

## Dispositivos y sesiones

- Consulta los dispositivos con sesión iniciada en `/settings/devices`
- Después de iniciar sesión en un dispositivo o entorno nuevo, **los retiros pueden bloquearse temporalmente** durante un tiempo (periodo de espera de seguridad)
- En ordenadores públicos, no confíes a largo plazo en extensiones desconocidas ni guardes códigos en lugares inseguros

***

## ¿Has perdido tu autenticador?

Si aún puedes acceder a tu email:

1. Inicia sesión con un código por email
2. Vuelve a vincular Authenticator (y las Passkeys que necesites) en Ajustes
3. Revisa la lista de dispositivos y elimina el dispositivo perdido

Si tampoco puedes acceder a tu email: contacta con soporte y prepara la documentación de verificación de identidad (según el proceso de soporte).
