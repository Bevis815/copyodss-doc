# Preguntas frecuentes

Cuando algo falle, consulta primero esta página. Si aun así no puedes resolverlo, ten preparados: tu email registrado, la hora de la acción, capturas de pantalla del error y el hash de la transacción o el ID del historial de operaciones.

---

## Cuenta e inicio de sesión

### ¿Los usuarios nuevos deben registrarse por separado?

En la mayoría de los casos, introducir un **email nuevo** en la página de inicio de sesión y completar el código crea una cuenta automáticamente. Si la pantalla aún pide un nombre / aceptar los términos, simplemente sigue las indicaciones.

### ¿No recibes el código de verificación?

Revisa tu carpeta de spam y la ortografía del email; vuelve a enviarlo cuando termine la cuenta atrás. A veces los servidores de correo corporativos lo bloquean: prueba con un email personal que uses a menudo.

### ¿Qué hago si falla la Passkey?

Inicia sesión con un código por email; asegúrate de que tu navegador sea compatible y de que no estés usando un WebView integrado incompatible, y luego vuelve a añadir la Passkey en Ajustes.

---

## Configuración de la cuenta y autorización

### ¿Necesito solicitar una cuenta de trading?

**No.** Normalmente se abre automáticamente tras iniciar sesión, así que puedes depositar de inmediato. En el caso poco frecuente de que muestre "aún no abierta", tócala para abrirla y acepta el acuerdo. Consulta [Cuenta de trading y estado de la página de billetera](wallet/trading-account.md).

### La página de billetera muestra "Agent authorization": ¿tengo que pagar gas?

No. Firmar es gratis y la plataforma cubre las comisiones on-chain. Solo necesitas la billetera con la que te registraste, conectada a **Polygon (chain ID 137)**.

### ¿Es un problema "Polymarket trading authorization incomplete"?

Solo toca **Re-authorize Polymarket**. Es un problema del paso de autorización y **no afecta a los fondos que ya has depositado**.

### ¿Por qué hay dos cifras, "saldo on-chain" y "saldo disponible"?

El saldo on-chain es el USDC nativo que realmente ha llegado; el saldo disponible es la parte procesada y lista para copiar. Pueden diferir durante unos minutos justo después de un depósito; es normal.

---

## Depósitos y saldo

### ¿Por qué no se ha actualizado mi saldo después de depositar?

Comprueba que: la red sea **Polygon o BSC (la que indica la página)**, el activo sea **USDC/USDT**, la dirección coincida exactamente con esta página y la transacción esté confirmada on-chain. BSC puede ser más lenta. Actualiza tu saldo tras la confirmación; si aún no ha llegado, proporciona el hash de la transacción.

### ¿Puedo depositar USDT?

Sí, pero debe ser USDT en la red seleccionada en la página, enviado únicamente a la dirección de esta página. No fuerces un retiro desde la red equivocada.

### ¿Qué pasa si la billetera de destino no tiene MATIC?

El retiro se completará, pero **después no podrás mover ese USDC on-chain**. Mantén un poco de MATIC (POL) en la dirección receptora.

### El retiro dice "channel busy" (canal ocupado): ¿qué debo hacer?

Espera unos minutos u horas según se indique y vuelve a intentarlo. **Tus fondos están seguros** y no necesitas volver a enviarlo.

### Justo después de llegar, ¿dice "automatically converting to tradable balance"?

Es normal. El USDC nativo que llega on-chain debe procesarse automáticamente para convertirse en saldo negociable: espera unos minutos y actualiza.

### ¿Puedo confirmar un retiro con una Passkey o un código por email?

**No.** Actualmente los retiros solo aceptan **códigos de Authenticator**; las Passkeys y los códigos por email son solo para el inicio de sesión y escenarios similares.

### ¿Desactivar Authenticator requiere un código?

Sí. Por seguridad, desactivarlo también requiere un código de 6 dígitos. Si vas a cambiar de dispositivo, es más fácil volver a vincularlo en el nuevo dispositivo.

### ¿Por qué el importe retirable es menor que mi saldo?

Las posiciones y las órdenes abiertas inmovilizan fondos. Guíate por **Max withdrawable** (máximo retirable).

### ¿Son iguales las direcciones de Polygon y BSC?

**No.** Nunca las confundas. Consulta [Redes compatibles](wallet/supported-networks.md).

---

## Gas y copia

### ¿Cuál es la diferencia entre el Gas de la plataforma y MATIC / BNB?

El Gas de la plataforma es un crédito de comisión de servicio de CopyOdds que se compra con USDC en la Gas Store. MATIC / BNB son tokens nativos on-chain usados para las comisiones de red: **no son lo mismo**.

### ¿Por qué no puedo añadir ni reanudar una regla de copia?

El motivo más común es **Gas = 0**. Compra Gas y luego activa / reanuda.

### ¿Cuánto USDC necesito para empezar a copiar?

Activar una regla normalmente solo requiere Gas > 0. Pero cada compra real necesita unos **$1** o más de USDC disponible.

### He comprado Gas / depositado fondos: ¿por qué sigue sin haber compras de copia?

Cuando los fondos son insuficientes, las compras se omiten, pero la regla no necesariamente se pausa. Después de recargar, ve a **My copies** (mis copias) y toca **Resume buys** (reanudar compras). Revisa también el historial de operaciones por si hay fallos de slippage, discrepancias de dirección o se alcanzó el límite de no aumentar posiciones.

---

## Ejecución de copias

### ¿Por qué algunas operaciones no se copiaron?

Motivos comunes: ajustes de dirección, importe demasiado pequeño, límite de no aumentar posiciones, slippage, USDC/Gas insuficiente, sin acciones que vender, liquidez insuficiente. Abre el historial de operaciones para ver el estado concreto.

### La actividad de copia muestra que el trader compró: ¿por qué yo no?

Actividad de copia ≠ tus ejecuciones. Revisa el historial de operaciones.

### El trader vendió: ¿por qué yo no?

Debes tener acciones en ese mercado. Si nunca compraste o ya vendiste todo, es normal que se omita la venta.

### ¿Cuál es la diferencia entre pausar y eliminar?

Una regla pausada se puede reanudar; una regla eliminada debe crearse de nuevo. Ninguna de las dos cierra automáticamente tus posiciones.

---

## Retiros y seguridad

### ¿Por qué los retiros requieren verificación reforzada?

Para proteger tus fondos e impedir que los activos se saquen directamente si se secuestra una sesión. Actualmente los retiros solo aceptan códigos de **Authenticator**; si no lo has configurado, actívalo primero en Ajustes. Las Passkeys y los códigos por email no se pueden usar para retiros.

### ¿Se puede usar una Passkey para retirar?

No. Una Passkey es un atajo para **iniciar sesión**; los retiros solo aceptan códigos de Authenticator.

### ¿No puedes retirar después de iniciar sesión en un teléfono nuevo?

Es posible que se haya activado un periodo de espera por dispositivo nuevo o que Authenticator aún no esté configurado en el nuevo entorno. Inténtalo más tarde y revisa la gestión de dispositivos y tu vinculación TOTP; contacta con soporte si sigue fallando.

### ¿El equipo oficial me pedirá alguna vez mi frase semilla?

**Nunca.** Consulta [Antiphishing](security/anti-phishing.md).

---

## Smart money

### ¿La clasificación garantiza ganancias?

**No.** Las métricas se basan en datos públicos y modelos e incluyen supuestos de simulación; rendimiento pasado ≠ rentabilidad futura.

### ¿Cómo abro el perfil de un trader?

`https://app.copyodds.io/@0xADDRESS` (añade `/zh` para la interfaz en chino).

### ¿Son "Copy fit / backtest P&L" mis rentabilidades reales?

No. Son principalmente simulaciones que asumen retraso + slippage; tus resultados reales están en el historial de operaciones.

---

## Modos de copia

### ¿Qué modos de copia hay y cuál debo elegir?

**Ratio** (por defecto), **By balance %** y **Fixed amount**. Si es tu primera vez, usa simplemente el **Ratio** por defecto: compras un porcentaje de lo que compre el trader, lo que hace que sea muy difícil que una de sus grandes apuestas arruine tu cuenta. Consulta [Los tres modos de copia](copy-trading/copy-modes.md).

### ¿Qué significa "Ratio"?

Si el trader compra $5,000 en una operación y tu ratio es del 10%, tú compras $500. El rango del ratio es 0.1%–100%.

### ¿Para qué sirve el "Leader order size range" (rango de tamaño de orden del líder) en el modo Ratio?

Filtra las órdenes diminutas (polvo) y las órdenes demasiado grandes. Las órdenes por debajo del límite inferior se omiten; las órdenes por encima del límite superior se siguen copiando, pero el importe se calcula como "límite superior × ratio", de modo que una gran apuesta del trader no se amplifica.

### ¿Puedo usar simplemente el "Suggested ratio" (ratio sugerido) que me da la página?

Sí. Se calcula como "tu saldo disponible ÷ (límite superior del rango × número aproximado de operaciones diarias del trader)", diseñado para que **uses aproximadamente esa cantidad de operaciones a lo largo de un día**. Redúcelo manualmente si quieres ser más conservador.

### ¿Por qué mi operación se omitió con "Outside size band"?

La orden del trader era demasiado pequeña (por debajo del límite inferior del rango). Es una orden de polvo filtrada a propósito, no un error.

### ¿Qué pasa si el importe calculado es inferior a $1?

Siempre que tu saldo sea suficiente, el sistema lo **completa automáticamente hasta $1** (la compra mínima del exchange) y coloca la orden en lugar de omitirla.

### ¿El slippage por defecto es del 30% o del 15%?

El valor por defecto en los ajustes de copia es **15%**, ajustable de 1% a 100%.

### ¿Por qué los parámetros aparecen rellenados cuando copio desde el perfil de un trader?

El sistema usa los resultados de la "simulación de copia" para rellenar por ti el slippage y el máximo de compras de copia; la página indicará "Pre-filled from copy simulation".

---

## Nuevas funciones

### ¿Cuál es la diferencia entre Leaderboard y Smart money?

Leaderboard muestra la **clasificación de ganancias diarias de las cuentas del copy pool** (página de inicio); Smart money muestra la **puntuación y el perfil de direcciones de traders individuales**. Para elegir traders, usa primero Leaderboard para encontrar una dirección y luego afina con los filtros de Smart money.

### ¿Son lo mismo "Copy activity" y "Trade history"?

No. Copy activity muestra **lo que hizo el trader**; Trade history muestra **los resultados de tus intentos de copia**. Comparar ambos es la forma más fácil de detectar problemas.

### ¿El copy trading simulado usa mi dinero real?

**No.** El copy trading simulado funciona en una cuenta virtual separada y tampoco necesita Gas.

### ¿Por qué no puedo vender mi posición?

Puede estar "pendiente de liquidación" (el mercado ha terminado y está esperando liquidarse), o puede que en ese momento no haya órdenes de compra en ese mercado. Si ganaste, aparecerá un botón **Redeem** (canjear).

### ¿Es el "Transaction history" de la página de billetera lo mismo que el menú de historial de operaciones?

No. **Executions** en el menú es tu **historial de operaciones de copia**; **Transaction history (`/wallets/ledger`)** en la billetera es tu **registro de movimientos de fondos y gasto de Gas**.

### ¿Eliminar un dispositivo en la gestión de dispositivos afectará a mis copias?

No eliminará tus reglas de copia, pero las sesiones del dispositivo antiguo se invalidan de inmediato y tendrá que volver a iniciar sesión.

### ¿La comisión en la página de afiliados es siempre del 10%?

No. Tu tasa de comisión depende de tu **nivel** (desde L1 con 10% hasta el nivel más alto). L1 se activa automáticamente después de que realices una compra; luego subes de nivel automáticamente según tu número de referidos directos; el nivel más alto debe comprarse.

### ¿Tengo que descargar la App en mi teléfono?

No. La versión web tiene todas las funciones; para una experiencia más parecida a una app, usa la opción "Añadir a pantalla de inicio" de tu navegador. Consulta [Usar CopyOdds en el móvil](getting-started/mobile-app.md).

---

## Aviso de riesgos

- Los precios del mercado fluctúan y el copy trading puede generar pérdidas
- La copia automatizada puede desviarse del trader debido al slippage, el retraso y la liquidez
- Una cadena, dirección o token equivocados pueden hacer que los fondos no lleguen o no se puedan recuperar
- Un Gas / USDC insuficiente hace que se omitan las compras
- Los resultados de la clasificación y de la simulación son solo de referencia y no constituyen una promesa de rentabilidad

Los usuarios nuevos deberían recorrer primero todo el flujo con una cantidad pequeña: Depositar → Comprar Gas → Copiar → Revisar el historial de operaciones → Luego probar un pequeño retiro.
