# Comment fonctionne le copy trading

Une fois la copie activée, CopyOdds **tente** de passer des ordres dans votre compte de trading selon vos règles chaque fois qu'un trader que vous suivez obtient une exécution.

**C'est Trade history qui indique si une copie a réussi** ; Copy activity ne montre que les actions publiques du trader.

![Historique des trades](../.gitbook/assets/change_doc.png)

***

## Processus d'exécution

1. Détection de l'exécution publique (achat / vente) du trader sur Polymarket
2. Recherche de votre règle de copie pour cette adresse et vérification que la direction correspond
3. Calcul du montant notionnel cible à partir d'un **montant fixe** ou d'un **pourcentage de vos USDC disponibles**
4. Tentative de passage de l'ordre dans la limite de votre tolérance au slippage
5. En cas d'exécution, déduction du **Gas de la plateforme** correspondant (environ 0.5% du notionnel) et mise à jour des positions / enregistrements

***

## Exécuté vs Ignoré vs Échoué

| Résultat | Signification |
|--------|---------|
| **Filled** | L'ordre de copie a été exécuté |
| **Skipped** | Aucun ordre n'a été passé en raison des paramètres, des fonds, etc. (fréquent) |
| **Failed** | L'ordre a été rejeté ou a rencontré une erreur |
| **Settled, etc.** | États de règlement / terminés tels qu'affichés par les filtres de l'interface |

### Raisons d'ignorance courantes

- Direction incompatible (Buy only / Sell only)
- Montant inférieur à l'achat minimum d'environ **$1**
- **Max open copy buys** atteint (1 par défaut = pas de renforcement des positions)
- Slippage trop important
- **Gas insuffisant** ou **USDC insuffisants**
- Le trader a vendu mais vous ne détenez pas la position correspondante
- Aucune contrepartie sur le marché pour le moment

***

## Que deviennent les règles lorsque les fonds manquent ?

| Situation | Statut de la règle | Achats | Ventes (si vous détenez des positions) |
|-----------|-------------|------|---------------------------------|
| Gas = 0 | Généralement toujours « en cours » ; une alerte de financement peut apparaître | Ignorés | Peuvent toujours être copiées |
| Pas assez d'USDC pour acheter | Comme ci-dessus | Ignorés | Peuvent toujours être copiées |
| Mise en pause manuelle | Manually paused | Non copiés | Non copiées |

Après avoir rechargé le Gas / les USDC, allez dans **My copies** (mes copies) et appuyez sur **Resume buys** (reprendre les achats) (si toute la règle a été mise en pause manuellement, appuyez plutôt sur Resume).

***

## Copy activity vs Trade history vs Positions

| Page | Contenu |
|------|---------|
| Copy activity | Les achats et ventes publics du trader |
| Trade history | Vos tentatives de copie et leurs résultats |
| Positions | Vos positions actuelles ; clôturer / récupérer les parts réglées |
| Daily P&L | Courbe du P&L réalisé par jour de trading |

Le P&L réalisé du jour est généralement réinitialisé chaque jour à heure fixe dans le fuseau horaire de votre compte (par ex. 8:00 AM) ; consultez la description dans l'App pour plus de précisions.
