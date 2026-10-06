# Redes compatibles

Los depósitos y los retiros admiten **redes diferentes**. Elige siempre exactamente lo que muestra la página para evitar que los fondos no lleguen.

***

## Resumen

| Acción | Redes compatibles | Activos | Tipo de dirección |
|--------|--------------------|--------|--------------|
| **Depósito** | **Polygon (PoS)**, **BSC** (cuando está habilitada) | USDC / USDT | Dirección diferente para cada red |
| **Retiro** | **Solo Polygon (PoS)** | **USDC** | Tu propia dirección receptora |

Ejemplos de redes no compatibles para depósitos: **la red principal de Ethereum, Arbitrum, Optimism**, etc. (a menos que el producto las añada explícitamente en el futuro).

***

## Polygon (PoS)

| Elemento | Descripción |
|------|-------------|
| Depósito | Compatible; la dirección que se muestra es la dirección de tu billetera custodiada (Custodial address) |
| Activos | USDC, USDT |
| Retiro | La **única** red de retiro; retira USDC a una dirección que pueda recibir USDC en Polygon |

La mayoría de los usuarios prefieren Polygon: el recorrido es más directo y coincide con la red de retiro.

***

## BSC

| Elemento | Descripción |
|------|-------------|
| Depósito | Compatible (cuando el puente / la red del producto está habilitado) |
| Activos | USDC, USDT |
| Dirección | **Dirección puente**, diferente de la dirección de Polygon |
| Retiro | **No se admite** retirar de CopyOdds a BSC |

Al retirar desde un exchange a través de BSC, cambia primero la página de depósito a BSC y luego copia la dirección. La llegada puede tardar unos minutos más.

***

## Errores comunes

| Error | Consecuencia |
|---------|-------------|
| Retirar en BSC pero copiar la dirección de Polygon | Puede no acreditarse / ser difícil de recuperar |
| Retirar en Polygon pero copiar la dirección de BSC | Igual que arriba |
| Enviar USDC de Ethereum | Normalmente no se acredita automáticamente |
| Introducir la dirección de la página de depósito como dirección de retiro | Los fondos pueden volver al lado custodiado y causar confusión; los retiros deben ir a **tu propia** dirección externa |
| Esperar poder retirar a BSC | Actualmente los retiros solo admiten USDC en Polygon |

***

## Reglas prácticas

1. **Elige primero la red y luego copia la dirección**
2. **Deposita en Polygon y retira en Polygon: lo más sencillo**
3. **BSC es solo para depósitos; no puedes retirar a BSC desde esta App**
4. **Usa solo la dirección de la página oficial + la función Verify deposit address**
