# Documentación de CopyOdds

CopyOdds es una plataforma de **análisis de smart money + copy trading automatizado** construida sobre [Polymarket](https://polymarket.com): descubre traders de mercados de predicción con un historial sólido y replica automáticamente sus ejecuciones en una cuenta de trading custodiada.

Esta documentación refleja la interfaz y los flujos actuales de la App (`app.copyodds.io`). Los nombres de botones y menús coinciden con la interfaz en inglés de la App.

## Empieza en cuatro pasos

1. **Inicia sesión / Regístrate** — Código por email, Passkey o Telegram
2. **Deposita** — Envía USDC / USDT en Polygon o BSC a tu dirección custodiada
3. **Compra Gas de la plataforma** — Créditos de comisión de servicio para el copy trading automatizado (no es MATIC on-chain)
4. **Copia** — Elige un trader en **Leaderboard** o **Smart money** → toca **Follow** (seguir) → elige un modo de copia (por defecto: **Ratio**) → guarda la regla

¿No sabes por dónde empezar? Comienza con el [Recorrido por la App](getting-started/app-tour.md).

## Antes de empezar a copiar

| Elemento | Requisito |
|------|-------------|
| Gas de la plataforma | **Mayor que 0** (de lo contrario no puedes activar la copia; las compras se omiten cuando se agota el Gas) |
| Saldo en USDC | Se recomienda al menos unos **$1**, para las compras reales |
| Cuenta de trading | Normalmente se abre automáticamente tras iniciar sesión |

## Accesos principales (según la navegación de la App)

| Función | Ruta / Navegación |
|---------|-------------------|
| Clasificación (ganancia diaria del copy pool) | **Leaderboard** → `/` (página de inicio) |
| Smart money | **Smart money** → `/smart-money` |
| Mis copias | **My copy trading** → `/copy-rules` |
| Actividad de copia | **Copy activity** → `/feed` |
| Copy trading simulado | **Simulation copy trading** → `/copy-trading/simulation` |
| Mis posiciones | **My positions** → `/executions/positions` |
| Historial de operaciones / P&L | **Executions** → `/executions/records`, `/executions/daily-pnl` |
| Tienda de Gas de la plataforma | **Store** → `/store` |
| Programa de afiliados | **Affiliation** → `/affiliate` |
| Depósito / Retiro | **Deposit / Withdraw** → `/wallets/deposit`, `/wallets/withdraw` |
| Perfil (resumen de activos) | **Profile** → `/profile` |
| Historial de transacciones | **Transaction history** → `/wallets/ledger` |
| Ajustes y seguridad | **Settings** → `/settings` |
| Dispositivos y Passkeys | **Settings → Devices** → `/settings/devices` |
| Descarga móvil | **Mobile App** → `/mobile-app` |
| Guía del usuario | **User guide** → `/help` |

## Orden de lectura sugerido

1. **Primeros pasos** (qué es → Inicio rápido → Recorrido por la App)
2. **Clasificación / Smart Money** (elige traders; revisa la puntuación y el drawdown)
3. **Copy trading** (cómo empezar, gestionar y revisar copias)
4. **Billetera** (depósito, Gas, retiro, historial de transacciones)
5. **Cuenta y ajustes, Seguridad** (mantén tu cuenta segura)
6. **Afiliados** (cuando quieras ganar compartiendo)

## Sobre esta documentación

- Esta documentación solo describe cómo usar el producto y **no constituye asesoramiento de inversión**.
- La interfaz se actualiza continuamente. Si las capturas de pantalla difieren ligeramente de tu versión, guíate por lo que muestra la App.

## Contactar con soporte

Ten preparados: tu email registrado, la hora de la acción, capturas de pantalla del error y el ID / estado / hash on-chain correspondiente de **Trade history** (historial de operaciones).
