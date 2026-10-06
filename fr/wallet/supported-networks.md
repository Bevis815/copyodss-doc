# Réseaux pris en charge

Les dépôts et les retraits prennent en charge **des réseaux différents**. Choisissez toujours exactement ce qu'indique la page pour éviter que les fonds n'arrivent pas.

***

## Vue d'ensemble

| Action | Réseaux pris en charge | Actifs | Type d'adresse |
|--------|--------------------|--------|--------------|
| **Dépôt** | **Polygon (PoS)**, **BSC** (lorsqu'il est activé) | USDC / USDT | Adresse différente selon le réseau |
| **Retrait** | **Polygon (PoS) uniquement** | **USDC** | Votre propre adresse de réception |

Exemples de réseaux non pris en charge pour les dépôts : **Ethereum mainnet, Arbitrum, Optimism**, etc. (sauf si le produit les ajoute explicitement à l'avenir).

***

## Polygon (PoS)

| Élément | Description |
|------|-------------|
| Dépôt | Pris en charge ; l'adresse affichée est l'adresse de votre portefeuille en garde (Custodial address) |
| Actifs | USDC, USDT |
| Retrait | Le **seul** réseau de retrait ; retirez des USDC vers une adresse capable de recevoir des USDC sur Polygon |

La plupart des utilisateurs préfèrent Polygon : le parcours est plus direct et correspond au réseau de retrait.

***

## BSC

| Élément | Description |
|------|-------------|
| Dépôt | Pris en charge (lorsque la passerelle / le réseau du produit est activé) |
| Actifs | USDC, USDT |
| Adresse | **Adresse de passerelle**, différente de l'adresse Polygon |
| Retrait | Le retrait de CopyOdds vers BSC **n'est pas pris en charge** |

Lorsque vous retirez depuis une plateforme d'échange via BSC, basculez d'abord la page de dépôt sur BSC, puis copiez l'adresse. L'arrivée des fonds peut prendre quelques minutes de plus.

***

## Erreurs courantes

| Erreur | Conséquence |
|---------|-------------|
| Retirer sur BSC mais copier l'adresse Polygon | Peut ne pas être crédité / difficile à récupérer |
| Retirer sur Polygon mais copier l'adresse BSC | Comme ci-dessus |
| Envoyer des USDC Ethereum | Généralement pas crédité automatiquement |
| Saisir l'adresse de la page de dépôt comme adresse de retrait | Les fonds peuvent revenir côté garde et créer de la confusion ; les retraits doivent aller vers **votre propre** adresse externe |
| S'attendre à pouvoir retirer vers BSC | Les retraits ne prennent actuellement en charge que les USDC sur Polygon |

***

## Règles de base

1. **Choisissez d'abord le réseau, puis copiez l'adresse**
2. **Déposer sur Polygon, retirer sur Polygon — le plus simple**
3. **BSC sert uniquement aux dépôts ; vous ne pouvez pas retirer vers BSC depuis cette App**
4. **N'utilisez que l'adresse de la page officielle + la fonctionnalité Verify deposit address**
