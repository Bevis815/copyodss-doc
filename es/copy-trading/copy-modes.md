# Los tres modos de copia (los principiantes empiezan aquí)

Lo primero que hay que elegir en los ajustes de copia es el **modo de copia**. Actualmente hay tres:

| Modo | Resumen en una línea | Ideal para |
|------|------------------|----------|
| **Ratio** (nuevo, por defecto) | Compras un **porcentaje fijo** de lo que compre el trader | La mayoría de las personas, especialmente cuando los tamaños de orden del trader varían mucho |
| **By balance %** | Cada operación usa un **porcentaje de tu propio saldo** | Quienes quieren que el tamaño de la posición se ajuste automáticamente a su saldo |
| **Fixed amount** | Cada operación compra **el mismo importe** | Traders cuyos tamaños de orden son bastante constantes |

> **Los usuarios nuevos usan el modo Ratio por defecto.** Es el modo más recomendado actualmente y se explica con más detalle a continuación.

***

## ¿Por qué se añadió el modo Ratio?

El importe fijo tiene un problema habitual: el trader compra $30 una vez y $3,000 la siguiente, pero tú siempre copias $10, así que pierdes por completo su ritmo: o copias demasiado poco para que importe o copias a ciegas demasiado.

El modo Ratio lo cambia a: **coloque lo que coloque, tú colocas un importe proporcional**.

| Ejecución del trader | Tu modo Fixed amount | Tu modo Ratio (10%) |
|---------------|------------------------|-----------------------|
| $50 | Copias $10 | Copias $5 |
| $500 | Copias $10 | Copias $50 |
| $5,000 | Copias $10 | Copias $500 |

La ventaja es que **sigue de forma natural el dimensionamiento de posiciones del trader**, sin que una gran apuesta ocasional suya arruine tu cuenta.

***

## El modo Ratio en detalle

### Tres cosas que configurar

| Ajuste | Dónde | Descripción |
|---------|-------|-------------|
| **Copy ratio** (ratio de copia) | Control deslizante bajo el modo | 0.1%–100%. Ejecución del trader × este ratio = el importe de tu orden |
| **Leader order size range** (rango de tamaño de orden del líder) | Segundo control deslizante bajo el modo | Solo copia las órdenes de "tamaño normal" del trader, filtrando las órdenes de polvo y las demasiado grandes |
| **Slippage tolerance** (tolerancia de slippage) | Bajo el modo | 1%–100%, por defecto **15%** |

### 1. Ratio de copia

Es el ratio de "cuánto copiar". La página de ajustes muestra una línea de vista previa:

> Líder 100, tú pones 10%, así que lo tuyo es 10.

La página normalmente también muestra un **Suggested ratio** (ratio sugerido) junto a "unas N operaciones/día". Se calcula así:

> **Ratio sugerido ≈ tu saldo disponible ÷ (límite superior del rango × número aproximado de operaciones diarias del trader)**

Ejemplo: tienes $1,000 disponibles, el trader compra unas 5 veces al día y el límite superior del rango es $800.
Ratio sugerido ≈ 1000 ÷ (800 × 5) = 25%. En otras palabras, **usarás aproximadamente el equivalente a 5 operaciones a lo largo de un día**, y una orden grande no agotará tu saldo de golpe.

Si no quieres el valor sugerido, simplemente arrastra el control deslizante para fijar el tuyo, de 0.1% a 100%.

> Consejo: una vez que arrastras el control deslizante, el sistema deja de sobrescribir automáticamente tu elección; la sugerencia solo se recalcula cuando actualizas o vuelves a elegir un trader.

### 2. Rango de tamaño de orden del líder

Este rango se deriva de **la mayor ejecución individual histórica del trader** y, por defecto, abarca la parte central (aproximadamente 5%–95%). Filtra dos tipos de órdenes:

| Situación | Tratamiento | Por qué |
|-----------|----------|-----|
| El trader compra **demasiado poco** (por debajo del límite inferior) | **Se omite**, no se copia | Estas "órdenes de polvo" no merecen copiarse y solo costarían Gas |
| El trader compra **dentro del rango** | Se copia normalmente según tu ratio | Es la actividad habitual del trader |
| El trader compra **demasiado** (por encima del límite superior) | **Se sigue copiando**, pero el importe se calcula como "límite superior × tu ratio" | Evita que una gran apuesta ocasional comprometa todo tu dinero |

La página tiene preajustes listos para usar:

| Preajuste | Significado | Ideal para |
|--------|---------|----------|
| **All 0–100%** | Sin ningún filtro | Traders cuyos tamaños de orden son muy regulares |
| **Balanced 1–99%** | Copia casi todo, filtrando solo los extremos | **Por defecto, lo mejor para principiantes** |
| **Core 20–80%** | Solo copia la parte central principal | Más conservador, copia solo la actividad principal |

**Ejemplo oficial**: rango $200–$800, ratio 10%, el trader compra $5,000 → solo copias $80.

> Consejo: justo después de elegir un trader, si aún no hay datos de sus ejecuciones históricas, la página indicará "No cache yet; copying at the default ratio for now, actual amounts will be capped by your balance" (todavía no hay caché; por ahora se copia con el ratio por defecto, los importes reales estarán limitados por tu saldo); es normal.

### 3. Tolerancia de slippage

- Significado: la desviación máxima permitida en el precio de ejecución
- Por defecto **15%**, ajustable de 1% a 100%
- **Más ajustada**: es más probable que se omita o falle cuando los precios se mueven
- **Más holgada**: es más probable que se ejecute, pero posiblemente a un precio peor

> Cuando empiezas a copiar desde el perfil de un trader, el sistema usa los resultados de la "simulación de copia" para rellenar el slippage y el máximo de compras de copia; la página indicará "Pre-filled from copy simulation".

***

## Cómo se calcula realmente una operación copiada

Supongamos que configuras: ratio **10%**, rango **$200–$800**, saldo $1,000.

| Paso | Descripción |
|------|-------------|
| 1. Mirar la ejecución del trader | Compró $5,000 |
| 2. Comprobar si está dentro del rango | Por encima del límite superior de $800, así que **no se omite**, pero se calcula a partir del límite superior |
| 3. Calcular el importe | Se toma el **menor** entre "ejecución del trader × 10%" y "límite superior × 10%" = $80 |
| 4. Comprobar tu saldo | Continúa si el saldo ≥ $1; si no es suficiente, se coloca la orden con lo que tu saldo realmente permita |
| 5. Completar hasta el mínimo | Si el resultado es inferior a $1, se **completa hasta $1** (la compra mínima del exchange) siempre que tu saldo lo permita |
| 6. Descontar Gas | Tras la ejecución, se descuenta aproximadamente un 0.5% en Gas de la plataforma |

Ahora un caso dentro del rango: el trader compra $500 → 500 × 10% = $50, se copia normalmente por $50.

***

## Cuándo se omiten las operaciones

| Mensaje en la App | En palabras sencillas | Qué hacer |
|--------------------|----------------|------------|
| **Outside size band** | La orden del trader era demasiado pequeña: una orden de polvo | Nada; es así por diseño |
| **Insufficient funds** | Tu saldo disponible es inferior a $1 | Deposita o reduce el ratio |
| **Your size < $1** | Demasiado pequeña incluso después de completarla | Aumenta el ratio o reduce el límite superior del rango |
| **Price ≥ $0.85** | El trader compró un resultado cuyo precio ya indica que es "casi seguro" | Nada |
| **Already open (no add-on)** | Ya has copiado en este mercado | Mantén el valor por defecto "sin aumentar" o cambia el ajuste |
| **Slippage too high** | El precio se alejó | Considera ampliar el slippage |
| **Low Gas** | Te has quedado sin Gas de la plataforma | Recarga en la [Gas Store](../wallet/gas.md) |

> Nota: la regla de **"por debajo de $1 se completa hasta $1"** se aplica en los tres modos (Ratio, Fixed amount, By balance %). Así que las órdenes inferiores a $1 no se omiten: se completan y se copian (siempre que tu saldo lo permita).

***

## Los otros dos modos

### By balance %

- Cada operación usa un **porcentaje de tu propio saldo disponible en USDC**; p. ej., al 5% con un saldo de $1,000, cada operación compra $50
- A medida que tu saldo crece, cada operación crece automáticamente; cuando disminuye, las operaciones se reducen
- Los resultados inferiores a $1 también se completan hasta $1

**Ideal para**: quienes quieren que el tamaño de la posición se ajuste a su saldo sin tener que ajustar constantemente los importes a mano.

### Fixed amount

- Cada operación compra **el mismo importe**, p. ej., $25 cada vez
- Mínimo $1
- Regla especial para órdenes pequeñas: cuando el importe es inferior a $1, si son **≥ 5 acciones** la orden usa el importe que configuraste; si son **menos de 5 acciones**, se ajusta automáticamente a $1

**Ideal para**: traders cuyos tamaños de orden son bastante constantes (p. ej., unos $200 por operación a largo plazo), cuando quieres un control preciso del coste de cada operación.

***

## ¿Cuál debo elegir?

| Tu situación | Recomendación |
|----------------|----------------|
| Primera vez, no sabes qué elegir | **Ratio** (por defecto) |
| Los tamaños de orden del trader varían mucho | **Ratio** |
| Quieres un control preciso del importe de cada operación | **Fixed amount** |
| Quieres que el tamaño de la posición se ajuste a tu saldo | **By balance %** |

***

## Preguntas frecuentes

**¿Cuánto es lo máximo que se me puede cobrar por operación en el modo Ratio?**

No hay un límite por operación aparte: tu ratio × la ejecución del trader es el importe, pero está limitado tanto por el "límite superior del rango" como por "tu saldo". Para ser más conservador, reduce el ratio y el límite superior del rango.

**Me pone nervioso usar directamente el ratio sugerido.**

Puedes usarlo directamente; el sistema ya tiene en cuenta "aproximadamente cuántas operaciones al día". Para ir más sobre seguro, empieza con una regla pequeña con un ratio más bajo, observa durante un día o dos si hay muchas omisiones y luego auméntalo gradualmente.

**¿El modo Ratio entra en conflicto con "sin aumentar posiciones"?**

No. El valor por defecto "máximo 1 compra de copia" (sin aumentar) significa que en **el mismo mercado** solo se compra una vez; el ratio controla **cuánto compra esta operación**. Para aumentar posiciones, sube "Max open copy buys" en los ajustes avanzados: **el máximo es All (ilimitado)**.

**¿El slippage por defecto en los ajustes es del 30% o del 15%?**

Ahora es del **15%**, ajustable de 1% a 100%.

**¿Hay también una "Ratio guide" oficial en la App?**

Sí. Toca **Ratio guide** en la esquina superior derecha del modo Ratio (o en la página de ajustes) para abrirla. Es la versión detallada propia de la plataforma; esta página es la explicación completa para principiantes.

***

## Páginas relacionadas

- Recórrelo paso a paso: [Cómo copiar a un trader](how-to-follow.md)
- Qué significa cada parámetro: [Ajustes de copia](settings.md)
- Cómo gestionarlo después de activarlo: [Gestionar copias](managing.md)
- Pruébalo primero sin gastar dinero: [Copy trading simulado](simulation.md)
