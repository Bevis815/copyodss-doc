# Gas de la plateforme

Le **Gas de la plateforme** est un **crédit de frais de service** de votre compte CopyOdds, utilisé pour payer les frais sur les exécutions copiées automatiquement.

> **Gas de la plateforme ≠ gas on-chain.** Il ne s'agit pas de MATIC, de POL ni de BNB, ni du gas que vous utilisez dans un portefeuille pour payer les frais de réseau.

Accès : **Gas Store** → `/store`.

![Gas Store](../.gitbook/assets/store_doc.png)

***

## Pourquoi avez-vous besoin de Gas ?

Chaque exécution copiée (achat ou vente) déduit des crédits de frais de service en fonction du montant notionnel de l'exécution. Sans Gas :

- **Vous ne pouvez pas créer ni reprendre de règles de copie**
- Dans le cadre des règles existantes, **les achats sont généralement ignorés**
- Si vous détenez encore des positions, **les ventes peuvent toujours être copiées** (les règles restent souvent actives)

***

## Frais (conditions actuelles du produit)

| Élément | Description |
|------|-------------|
| Frais | **Les achats comme les ventes** coûtent environ **0.5%** du montant réellement exécuté, déduit en Gas |
| Conversion | Environ **1 USDC = 100 Gas** |
| Exemple | Une exécution de $100 consomme environ **50 Gas** (l'achat et la vente sont chacun facturés une fois) |
| Source de paiement | Les forfaits sont payés à partir de votre **solde USDC disponible** en garde |
| Retirable ? | **Non** — ne peut être ni retiré ni transféré |

Consultez la page de la boutique pour les forfaits actuels et les éventuels bonus (comme les bonus liés au niveau de parrainage).

> Si vous avez des ordres non terminés, des positions ouvertes ou des retraits en attente, la boutique peut temporairement **ne pas autoriser l'achat de Gas avec votre solde** et vous inviter à régler la situation sur la page Portefeuille ; une fois réglée, vous pouvez acheter normalement.

***

## Comment acheter

1. Ouvrez le Gas Store et assurez-vous d'avoir suffisamment d'USDC
2. Lisez la description des frais
3. Choisissez un forfait → confirmez le paiement
4. Le Gas est crédité instantanément
5. Si des achats ont été ignorés auparavant faute de Gas : allez dans **My copies** (mes copies) et appuyez sur **Resume buys** (reprendre les achats)

***

## Gas vs USDC

| | USDC | Gas de la plateforme |
|--|------|--------------|
| Objectif | Capital de copie | Frais de service de copie |
| Comment l'obtenir | Dépôt on-chain | Achat avec des USDC dans la boutique |
| Peut-il être retiré on-chain ? | Oui (voir Retrait) | Non |

***

## FAQ

**Dois-je faire quelque chose après avoir acheté du Gas ?**  
Nous vous recommandons d'aller dans **My copies** et d'appuyer sur **Resume buys** pour lever toute alerte de financement.

**Mes règles s'arrêteront-elles lorsque le Gas sera épuisé ?**  
En général, la règle entière n'est pas mise en pause — les achats sont ignorés, et les ventes peuvent toujours être copiées si vous détenez des positions.
