# Cómo copiar a un trader

Añade una dirección de smart money a la copia automatizada y guarda la regla.

![Asistente de copia](../.gitbook/assets/follow_doc.png)

***

## Lista de comprobación previa

| Condición | Notas |
|-----------|-------|
| Sesión iniciada con una cuenta de trading activa | Normalmente se abre automáticamente tras iniciar sesión |
| Gas de la plataforma > 0 | **Obligatorio**; de lo contrario no puedes activar / reanudar |
| Saldo disponible en USDC | Se recomienda unos $1 o más; de lo contrario es probable que se omitan las compras |

***

## Accesos

Cualquiera de los siguientes:

1. Toca **Follow** (seguir) en la lista de **Smart money** o en una página de perfil
2. **Quick copy / New copy** en **My copies** (mis copias)
3. Abre `/copier` (Quick copy) directamente y pega una dirección
4. Abre un enlace de perfil `https://app.copyodds.io/@0x...` y toca Follow

***

## Pasos

1. Confirma la **Leader address** (dirección del líder) (0x…); traerla desde la clasificación evita errores tipográficos
2. Opcional: ponle nombre a la regla (Name this copy trade)
3. Elige un **Copy mode** (modo de copia): elige uno de tres:
   - **Ratio** — **El modo por defecto**; copia un porcentaje fijo de cada ejecución del líder (el líder compra $500 con un ratio del 10% → tú compras $50)
   - **By balance %** — Un porcentaje de **tu USDC disponible** (1%–100%)
   - **Fixed amount** — Compra el mismo importe cada vez (mínimo $1)
4. Configura **Slippage tolerance** (tolerancia de slippage): por defecto **15%**, ajustable de 1% a 100%

   > Para saber en qué se diferencian los tres modos, cómo se calcula el ratio y de dónde salen los valores sugeridos, consulta [Los tres modos de copia](copy-modes.md)
5. Opcionalmente, abre **Advanced settings** (ajustes avanzados):
   - **Direction**: Both / Buy only / Sell only (ambas / solo compra / solo venta)
   - **Max open copy buys**: por defecto **1** (sin aumentar posiciones); el máximo es **All (ilimitado)**
6. Guarda (**Copy trade / Save**)
7. Ve a **My copies** y confirma que el estado sea **Following** (siguiendo)

***

## Importe fijo vs. % del saldo

| Modo | Comportamiento | Ideal para |
|------|----------|----------|
| Importe fijo | Tanto si el trader compra $50 como $500, tú copias con el importe que configuraste | Controlar el riesgo por operación |
| % del saldo | Copia las compras con un % de tu saldo disponible en ese momento | Ajustarse automáticamente a tu capital |

Si el importe calculado a partir del porcentaje está por debajo del tamaño mínimo de orden, el sistema puede elevarlo al mínimo antes de intentarlo.

***

## Notas

- Cada dirección líder normalmente solo tiene un conjunto de ajustes activo; volver a guardar lo sobrescribe
- Cambiar una regla solo afecta a las copias futuras y no reescribe las ejecuciones pasadas
- Detener / eliminar una regla **no** vende automáticamente tus posiciones
- Prueba primero con un importe pequeño y solo auméntalo cuando el historial de operaciones parezca normal

***

## Dónde mirar después de copiar

| Lo que quieres ver | Adónde ir |
|----------------------|-------------|
| Lo que el trader acaba de hacer y si lo copié | [Actividad de copia](copy-activity.md) |
| Lo que tengo actualmente | [Mis posiciones e historial de operaciones](positions-and-records.md) |
| Estado de la regla, pausar / reanudar | [Gestionar copias](managing.md) |
