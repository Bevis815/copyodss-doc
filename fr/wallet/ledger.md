# Historique des transactions

**Transaction history** (historique des transactions) enregistre chaque mouvement de fonds entrant et sortant de votre compte, ainsi que les dépenses de Gas — considérez-le comme un relevé bancaire.

Accès : **Transaction history** → `/wallets/ledger` (généralement accessible depuis les pages de dépôt / retrait)

***

## Champs du tableau

| Champ | Signification |
|-------|---------|
| **Network / Asset** | par ex. Polygon (PoS) + USDC, BSC + USDT, Platform + Gas |
| **Type (In / Out)** | Entrant ou sortant |
| **Status** | Received, Completed, Posted |
| **Balance after** | Ce qui reste sur le compte après cette opération |
| **View on-chain** | Ouvrir cette transaction dans un explorateur de blocs |

Trois types d'enregistrements :

| Type | Description |
|------|-------------|
| **Dépôt** | USDC / USDT transférés depuis un portefeuille externe |
| **Retrait** | Envoyé vers votre propre adresse |
| **Dépense de Gas** | Crédits de frais de service déduits pour chaque exécution copiée |

***

## Quand les chiffres ne concordent pas

| Symptôme | Ce qu'il faut vérifier |
|---------|---------------|
| Dépôt non affiché | Le réseau était-il correct, l'actif est-il de l'USDC/USDT, l'adresse correspond-elle exactement à celle de la page pour ce réseau, la transaction est-elle confirmée on-chain (BSC est plus lent) ? |
| Retrait bloqué sur « Processing » | Vous devez d'abord effectuer la vérification renforcée du retrait ; un délai de carence peut s'appliquer après un nouvel appareil ou un changement lié au risque |
| Plus de Gas déduit que prévu | Chaque achat et chaque vente est facturé environ 0.5% du montant exécuté ; comparez avec l'exemple de [Gas de la plateforme](gas.md) |
| Le solde ne correspond pas aux positions | Les positions et les ordres ouverts immobilisent des fonds ; fiez-vous au **Max withdrawable** |

Si vous ne trouvez pas l'opération, envoyez au support l'**heure, le montant et le statut** figurant dans le registre, ainsi que le hash on-chain.
