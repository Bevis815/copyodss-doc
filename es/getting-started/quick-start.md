# Inicio rápido

Sigue estos pasos para pasar de abrir la App a tu primera regla de copia. Usa siempre los dominios oficiales **copyodds.io / app.copyodds.io**.

![Página de inicio de sesión](../.gitbook/assets/login_doc.png)

***

## 1. Inicia sesión o crea una cuenta

1. Abre la App y ve a **Login** (iniciar sesión).
2. Introduce tu email → **Send code** (enviar código) → introduce el código de 6 dígitos → inicia sesión.
3. **Un email nuevo crea una cuenta automáticamente** (no hay una página de registro aparte con tu nombre; si la pantalla aún pide un nombre / aceptar los términos, simplemente sigue las indicaciones).
4. Opcional: inicia sesión con una **Passkey** o con **Telegram**.
5. Si llegas a través de un enlace de invitación, el código de invitación normalmente se rellena automáticamente.

### Notas

- Los códigos suelen ser válidos durante unos 5 minutos; no puedes reenviarlos inmediatamente después de enviarlos
- Si el email no llega, revisa tu carpeta de spam / promociones
- Las Passkeys deben registrarse en un dispositivo y navegador compatibles (gestiónalas en Ajustes)

***

## 2. Deposita USDC / USDT

1. Abre **Assets / Deposit** (activos / depósito) → `/wallets/deposit`
2. **Elige una red**: Polygon (PoS) o BSC (debe coincidir con la red desde la que retiras en tu exchange)
3. **Elige un activo**: solo USDC o USDT
4. Copia la dirección de esta página o escanea el código QR para transferir (**las direcciones de Polygon y BSC son diferentes: nunca las confundas**)
5. Espera la confirmación on-chain; BSC puede tardar unos minutos más

![Página de depósito](../.gitbook/assets/usdc1_doc.png)

Consulta [Depósito](../wallet/deposit.md) y [Redes compatibles](../wallet/supported-networks.md) para más detalles.

***

## 3. Compra Gas de la plataforma

1. Abre **Gas Store** → `/store`
2. Comprueba tus saldos actuales de Gas y USDC
3. Elige un paquete → paga con tu USDC custodiado
4. El Gas se acredita al instante (no retirable)

![Gas Store](../.gitbook/assets/store_doc.png)

Comisiones en resumen: cada ejecución de copia cuesta aproximadamente un **0.5%** de su importe nocional en Gas; **1 USDC ≈ 100 Gas**. Consulta [Gas de la plataforma](../wallet/gas.md).

***

## 4. Elige un trader y cópialo

1. Abre la página de inicio **Leaderboard** (clasificación) o **Smart money** → `/` o `/smart-money`
2. Usa las categorías, los filtros rápidos o los filtros avanzados para elegir un trader
3. Toca **Follow** (seguir), o abre primero el perfil y síguelo desde allí
4. Elige un **modo de copia** (por defecto **Ratio**), el slippage y las opciones avanzadas
5. Asegúrate de que Gas > 0 y guarda → gestiónalo en **My copies** (mis copias)

![Smart money + Follow](../.gitbook/assets/smarket_doc.png)

![Ajustes de copia](../.gitbook/assets/follow_doc.png)

***

## 5. Comprueba si la copia funciona

| Página | Propósito |
|------|---------|
| **My copies** | Si la regla está activa y si hay una alerta de fondos |
| **Trade history** | Si tus órdenes se ejecutaron / se omitieron / fallaron |
| **Copy activity** | Las acciones públicas del trader (**no** tus ejecuciones) |
| **Positions** | Tus posiciones actuales; ciérralas / canjéalas aquí |

***

## Consejos para principiantes

- Empieza con un depósito pequeño, compra un poco de Gas y prueba con un importe fijo pequeño durante 1–2 días
- Cuando los fondos o el Gas escasean, las compras se omiten, pero la regla normalmente **no** se pausa automáticamente; después de recargar, ve a **My copies** y toca **Resume buys** (reanudar compras)
- Los retiros solo admiten **USDC en Polygon**: comprueba bien la dirección antes de enviar

***

## ¿No sabes a quién copiar? Dos enfoques seguros

1. **Consulta primero la clasificación** (página de inicio) para encontrar cuentas con un rendimiento reciente estable y luego verifica la puntuación y el drawdown en la página del perfil
2. **¿Sigues sin estar seguro? Prueba primero el [Copy trading simulado](../copy-trading/simulation.md)**: no implica dinero real

Cuando te sientas seguro, vuelve al paso 4 de esta página para empezar a copiar en real.
