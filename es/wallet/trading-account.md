# Cuenta de trading y estado de la página de billetera

Tu **cuenta de trading** de CopyOdds **normalmente se abre automáticamente tras iniciar sesión**, sin necesidad de solicitarla aparte. Es tu **billetera de trading custodiada**: el USDC / USDT que depositas se guarda aquí y se usa para el copy trading.

Acceso: **Wallets** → `/wallets` (la opción de menú **Deposit** abre esta página)

***

## Lo que verás normalmente

| Sección | Contenido |
|---------|---------|
| Dirección de depósito on-chain | Tu dirección de depósito (**diferente para cada red**); cópiala o guarda el código QR |
| Saldo disponible | La parte que puedes usar para copiar de inmediato |
| Saldo on-chain | El USDC nativo que realmente ha llegado a la blockchain |
| Gas de la plataforma | Se usa para pagar las comisiones de servicio del copy trading |
| Retiro | Introduce una dirección receptora de Polygon y un importe |
| Historial de transacciones | Depósitos, retiros y gasto de Gas |

Si ves todo esto, todo funciona correctamente y puedes depositar de inmediato.

***

## Por qué difieren los dos saldos

| Término | Significado |
|------|---------|
| **Saldo on-chain** | El USDC nativo que realmente ha llegado a la blockchain |
| **Saldo negociable** | La parte que la plataforma ha procesado y que se puede usar para copiar |

Si, justo después de un depósito, ves "xx native USDC on-chain, automatically converting to tradable balance" (xx USDC nativo on-chain, convirtiéndose automáticamente en saldo negociable), es **el flujo normal**: espera unos minutos y actualiza.

***

## Estados que puedes ver ocasionalmente

No todo el mundo los verá; si te aparecen, gestiónalos como se describe a continuación.

### "CopyOdds trading account not yet opened" (cuenta de trading de CopyOdds aún no abierta)

En casos poco frecuentes, la cuenta no se abre automáticamente (p. ej., algo falló durante la configuración). Toca **Open trading account** (abrir cuenta de trading), lee y marca el acuerdo y luego confirma.

Resumen del acuerdo:

| Cláusula | Contenido |
|--------|---------|
| Servicio | La plataforma crea para ti una billetera de trading custodiada, que se usa para depósitos, copias, órdenes y retiros |
| Custodia y autorización | Los activos están custodiados por la plataforma y no tienes la clave privada directamente; autorizas a la plataforma a realizar las firmas y la ejecución de operaciones necesarias |
| Protección de retiros | Es posible que se te pida activar la verificación reforzada con **Authenticator (TOTP)** antes de retirar |
| Fondos y redes | Envía solo activos compatibles a la dirección y la red que se muestran en la página; **elegir la red o el activo equivocados puede hacer que los fondos sean irrecuperables** |
| Aviso de riesgos | El copy trading es de **alto riesgo y puedes perder toda tu inversión**; el slippage, la liquidez y el retraso afectan a los resultados |
| Requisitos y cumplimiento | Debes tener al menos 18 años; no puede usarse para blanqueo de dinero, fraude ni otros fines ilegales |

> El acuerdo puede actualizarse; los términos completos están en el diálogo de la App y en las Condiciones de servicio para usuarios.

### Aparece una sección "Agent authorization"

Algunas cuentas ven una sección adicional de **Agent authorization** (autorización de agente) en la página de billetera. Te permite **autorizar con una sola firma**, tras lo cual la plataforma coloca órdenes por ti y **cubre el gas on-chain** (no necesitas tu propio MATIC).

Si ves esta sección, simplemente sigue las indicaciones:

| Requisito | Descripción |
|-------------|-------------|
| Firma con **la billetera con la que te registraste** | Elegir la cuenta equivocada en tu billetera muestra "Current wallet is not the registered wallet" |
| Cambia tu billetera a **Polygon (chain ID 137)** | De lo contrario verás "Please switch your wallet to Polygon and try again" |
| Completa la firma de una sola vez | Cerrar la extensión o cambiar el contenido a mitad de proceso provoca un fallo; actualiza y empieza de nuevo |
| Vigila la caducidad | Cuando caduca, la copia se pausa: toca **Renew** (renovar); también puedes **Revoke** (revocar) la autorización (después de revocarla tendrás que volver a autorizar) |

Errores habituales: billetera equivocada / cadena equivocada / solicitud de autorización caducada / el contenido firmado no coincide con la verificación (normalmente por interferencia de una extensión: actualiza y vuelve a intentarlo).

### "Polymarket trading authorization incomplete" (autorización de trading de Polymarket incompleta)

Toca **Re-authorize Polymarket**. Este mensaje indica un problema en el paso de autorización y **no afecta a los fondos que ya has depositado**.

> En casos poco frecuentes en los que la autorización automática falla, la página ofrece la opción "Manually paste Polymarket API credentials (advanced)" (pegar manualmente las credenciales de la API de Polymarket, avanzado) para solucionar problemas. Los usuarios normales no necesitan tocarla.

***

## Preguntas frecuentes

**¿La cuenta de trading tiene alguna comisión?**  
Abrirla es gratis. El Gas de la plataforma, de aproximadamente un 0.5%, solo se descuenta cuando se ejecutan operaciones copiadas.

**¿Dónde está mi clave privada?**  
No la tienes tú. CopyOdds usa una billetera custodiada cuyas claves privadas la plataforma guarda de forma aislada; tú controlas tus fondos mediante el inicio de sesión + la verificación reforzada de retiros.

**¿Por qué puedo ver la dirección on-chain pero no puedo sacar fondos yo mismo?**  
Es el diseño custodiado: la dirección pertenece a la plataforma y se usa para recibir tus depósitos. Para sacar fondos, debes pasar por el flujo de **retiro** y completar la verificación reforzada.

**¿Cuándo difieren los dos saldos?**  
Normalmente solo durante los pocos minutos **justo después de un depósito, mientras se convierte automáticamente**. Si siguen siendo diferentes durante mucho tiempo, actualiza; si aún no cuadran, contacta con soporte con el hash de la transacción.
