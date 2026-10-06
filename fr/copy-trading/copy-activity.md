# Activité de copie

**Copy activity** (activité de copie) vous indique deux choses : **ce que le trader vient de faire** et **si vous l'avez copié**.

Accès : **Copy activity** → `/feed` (généralement accessible depuis **My copies** ou le menu)

***

## Contenu de la page

1. **En haut : les portefeuilles que je copie** — Liste les adresses pour lesquelles vous avez activé la copie ; appuyez sur l'une d'elles pour n'afficher qu'elle
2. **Trois onglets**

| Onglet | Contenu |
|-----|---------|
| **Activity** | Les achats / ventes publics du trader |
| **My orders** | Le résultat de chaque ordre que le système a passé pour vous |
| **My positions** | Vos positions actuelles et votre P&L |

3. **Filtres** : All / Successful / Buys / Sells / Copying
4. Chaque entrée affiche une heure (**just now**, **a few minutes ago**) ; sur mobile, tirez vers le bas pour actualiser

***

## Lire les statuts de copie

| Statut | Signification | Que faire |
|--------|---------|------------|
| **Copying** | Tentative de passage de l'ordre en cours | Patientez un instant |
| **Copied** | Copié avec succès | Rien |
| **Skipped** | Non copié cette fois | Vérifiez la raison de l'échec |
| **Failed** | L'ordre a été rejeté ou a rencontré une erreur | Vérifiez la raison — peut-être le solde / le slippage / le Gas |
| **Not copied** | Cette entrée ne fait pas partie de votre périmètre de copie | Rien |

Appuyez sur n'importe quelle entrée pour voir les **détails du trade** : marché, direction, adresse, volume, règle de copie, portefeuille de copie, statut, heure et hash de la transaction on-chain.

***

## Raisons d'ignorance courantes

- Direction incompatible (vous avez réglé Buy only / Sell only)
- Montant trop faible (inférieur à l'achat minimum de la plateforme d'échange, d'environ $1)
- « Max open copy buys » atteint (1 par défaut, c'est-à-dire pas de renforcement des positions)
- Slippage trop important
- **Gas insuffisant** ou **USDC insuffisants**
- Le trader a vendu mais vous ne détenez pas la position correspondante
- Personne ne prenait d'ordres sur ce marché à ce moment-là

***

## Conseils

- Utilisez **Activity** pour observer les autres et **Trade history** pour vous vérifier vous-même — comparer les deux est le moyen le plus simple de repérer les problèmes
- S'il y a beaucoup d'ignorances, vérifiez d'abord le Gas et le solde, puis envisagez d'ajuster le slippage ou de baisser le montant
- Lorsque vous partagez une entrée avec le support, indiquez l'**ID de l'enregistrement** ou le **hash de la transaction**
