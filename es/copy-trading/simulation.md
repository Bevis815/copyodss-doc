# Copy trading simulado

El **copy trading simulado** ejecuta tu estrategia de copia con una "billetera virtual": **sin dinero real**, solo para probar parámetros y ver resultados. Es ideal para principiantes que aún no están listos para invertir dinero real.

Acceso: **Simulation copy trading** → `/copy-trading/simulation`

> El copy trading simulado se está desplegando de forma gradual. Si no ves este menú, todavía no se ha habilitado para ti.

***

## En qué se diferencia de la copia real

| | Simulación | Copia real |
|--|------------|--------------|
| Dinero | Saldo virtual | Tu USDC custodiado |
| Gas | No se necesita | Se necesita (aproximadamente un 0.5% de comisión de servicio por operación) |
| ¿Puedes perder dinero? | No de verdad | Sí |
| Propósito | Probar parámetros, ver el rendimiento a largo plazo | Rentabilidad real |

***

## Empieza en tres pasos

### 1. Crea una cuenta virtual

Toca **Create virtual account** (crear cuenta virtual) y rellena:

| Campo | Descripción |
|-------|-------------|
| Nombre de la cuenta | Algo para diferenciarlas, p. ej., "Prueba-A" |
| Saldo inicial | Capital simulado |
| Duración (días) | Cuando expira, no se abren nuevas posiciones; las posiciones existentes aún pueden cerrarse o liquidarse |

### 2. Añade direcciones para copiar

Añade direcciones de traders en **Copy addresses** (direcciones de copia); puedes ponerle nombre a la estrategia y añadir notas.

### 3. Configura la estrategia

| Ajuste | Descripción |
|---------|-------------|
| Método de copia | Ratio / Fixed amount |
| Dirección | Compra y venta / Solo compra / Solo venta |
| Mín. / Máx. por operación | Rango de importe para cada operación |
| Límite por mercado | Lo máximo que se invierte en un solo mercado |
| Límite diario | Lo máximo que se invierte por día |
| Slippage máximo | No hay ejecución si se supera |
| Retraso de ejecución | Simula "reaccionar un poco más lento" |
| Enfriamiento por mercado | Intervalo mínimo entre dos copias en el mismo mercado |
| Pausa tras fallos consecutivos | Pausar tras este número de fallos seguidos (por defecto 10) |

Toca **Start simulation copy** (iniciar copia simulada) para ejecutarla.

***

## Ver los resultados: cinco pestañas

| Pestaña | Contenido |
|-----|---------|
| **Copy addresses** | Las direcciones que añadiste, los ajustes de la estrategia y el estado |
| **Positions** | Posiciones simuladas; puedes simular su cierre manualmente |
| **Executions** | Acciones, comisiones y estado de cada ejecución simulada |
| **Performance** | Curva de patrimonio, P&L total, tasa de acierto, drawdown máximo, coste de slippage, coste de comisiones, etc. |
| **Ledger** | Detalles de cada movimiento de fondos |

### Estados

| Estado de la cuenta | Significado |
|----------------|---------|
| Active | Funcionando con normalidad |
| Paused | La pausaste; se puede reanudar |
| Expired | Sin nuevas posiciones; el patrimonio existente aún se puede gestionar |
| Archived | Guardada; no se puede archivar mientras tenga posiciones |

### Nota sobre el cierre de posiciones

Cerrar manualmente requiere un **precio de mercado de los últimos 15 minutos** para obtener una cotización; si el precio está desactualizado o falta, se te pedirá que actualices la cotización. Antes de confirmar, verás el precio de ejecución estimado, el slippage, las comisiones, los ingresos estimados y el P&L estimado.

***

## En una frase

El verdadero valor del copy trading simulado es este: **antes de gastar dinero real, puedes ver a qué conduce realmente "copiar con frecuencia + slippage alto + capital pequeño".**
