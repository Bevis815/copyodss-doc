# Dispositivos y Passkeys

Esta página trata dos temas de seguridad: **qué dispositivos han iniciado sesión en tu cuenta** y **cómo iniciar sesión rápidamente con Face ID / huella dactilar**.

Acceso: Ajustes → Seguridad → **Devices** (dispositivos) → `/settings/devices`; las Passkeys se gestionan en Ajustes → `/settings/passkeys`

***

## 1. Dispositivos

### Lo que verás

| Campo | Significado |
|-------|---------|
| Nombre del dispositivo | p. ej., el modelo de tu teléfono o el nombre del sistema operativo; muestra "Unknown device" si no se puede identificar |
| **Current device** | El que estás usando ahora mismo |
| **Last active** | Cuándo se usó por última vez |
| Sesiones activas | Cuántas sesiones hay iniciadas en este dispositivo |
| Retiro disponible a partir de | Los dispositivos nuevos normalmente tienen que esperar un tiempo antes de poder retirar |

### Eliminar un dispositivo

1. Busca un dispositivo que no reconozcas → toca **Remove** (eliminar)
2. Después de confirmar, el dispositivo se elimina y **sus sesiones se invalidan de inmediato**

### Cuándo eliminar uno

- Has cambiado de teléfono / ordenador y el dispositivo antiguo sigue en la lista
- Hay un dispositivo en tu historial de inicios de sesión que no reconoces
- Sospechas que otra persona está usando tu cuenta

> Después de eliminarlo, ese dispositivo debe volver a iniciar sesión (código por email / Telegram / Passkey).

***

## 2. Passkeys

Una Passkey te permite iniciar sesión con **Face ID, la huella dactilar o el bloqueo de pantalla** de tu teléfono en lugar de introducir un código.

### Añadir una Passkey

1. Ajustes → Passkeys → **Add passkey** (añadir passkey)
2. Completa la verificación con Face ID / huella dactilar según se indique
3. Una vez hecho, la Passkey aparece en la lista con su fecha de creación, la fecha de último uso y si está sincronizada

### Usarla para iniciar sesión

Elige **Passkey** en la página de inicio de sesión: no se necesita email.

### Eliminar una Passkey

Selecciónala → **Delete** (eliminar) → confirma. Después de eliminarla, ese dispositivo ya no podrá iniciar sesión con una Passkey.

### Solución de problemas

| Síntoma | Qué hacer |
|---------|------------|
| Face ID no aparece al añadirla | Cancela y **vuelve a tocar "Add Passkey"**, completando la verificación en cuanto aparezca el aviso; cierra primero los banners de notificaciones |
| Indica que este dispositivo no es compatible | Usa el navegador integrado del sistema (Safari en iOS, Chrome en Android), o simplemente usa un código por email |
| Indica que ya existe una Passkey con el mismo nombre | Elimina primero la entrada antigua "Android device"; si usas un proxy / VPN, desactívalo y vuelve a intentarlo |
| El inicio de sesión falla | Inicia sesión con un código por email; un fallo de la Passkey no afecta a la seguridad de tu cuenta |

> Las Passkeys solo se pueden usar para iniciar sesión y **no se pueden usar para la verificación de retiros**.
