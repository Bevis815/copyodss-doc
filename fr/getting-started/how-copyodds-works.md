# Comment fonctionne CopyOdds

De « un trader obtient une exécution » à « votre compte tente de la copier », l'ensemble du processus se présente ainsi :

```text
Un trader smart money obtient une exécution sur Polymarket
        ↓
CopyOdds détecte l'exécution publique
        ↓
Correspondance avec votre règle de copie pour cette adresse
        ↓
Calcul de la taille de l'ordre selon la règle (montant fixe ou % de votre solde)
        ↓
Tentative de passage de l'ordre dans la limite du slippage (consomme du Gas de la plateforme)
        ↓
Le résultat est inscrit dans Trade history ; les avoirs apparaissent dans Positions
```

## 1. Découvrir des traders

- Le système note et sélectionne en continu les portefeuilles publics Polymarket
- Le **classement affiché** exige généralement que le score global atteigne un seuil (par ex. ≥ 40) ; les adresses à faible score peuvent en sortir
- Dans **Smart money**, vous pouvez parcourir, rechercher ou analyser des adresses non répertoriées (si la fonctionnalité est disponible, une limite quotidienne peut s'appliquer)

## 2. Les fonds et les frais sont séparés

| Ressource du compte | Objectif |
|---------------------|---------|
| **USDC (etc.)** | Capital de copie : utilisé lors des achats, restitué lors des ventes |
| **Gas de la plateforme** | Crédits de frais de service : environ 0.5% du montant notionnel est déduit par exécution copiée |

Lorsque le Gas est à 0 : vous **ne pouvez pas créer / reprendre de règles de copie**. Les règles existantes continuent généralement de fonctionner, mais **les achats sont ignorés** ; les ventes peuvent toujours être copiées si vous détenez des positions.

## 3. Comment les règles de copie s'appliquent

Vous enregistrez une règle par adresse de trader suivi (enregistrer à nouveau pour la même adresse l'écrase) :

- **Mode de copie** (choisissez-en un ; par défaut **Ratio**) :
  - **Ratio** : chaque exécution du trader × votre ratio = le montant de votre ordre
  - **By balance %** : chaque trade utilise un pourcentage de vos propres USDC disponibles
  - **Fixed amount** : chaque trade achète le même montant
  - Voir [Les trois modes de copie](../copy-trading/copy-modes.md)
- **Direction** : Les deux / Achat uniquement / Vente uniquement
- **Slippage** : pas d'exécution si le prix s'écarte trop (15% par défaut)
- **Ratio de copie / Plage de taille** (mode Ratio uniquement) : contrôle « combien copier » et « quelles tailles d'ordre copier »
- **Max open copy buys** (nombre maximal d'achats copiés ouverts) : 1 par défaut (pas de renforcement des positions) ; peut être augmenté, le maximum étant **All (illimité)**

Après avoir détecté une exécution du trader, le système tente de passer un ordre selon ces règles. Il **ne garantit pas** que chaque trade sera copié.

## 4. Comment savoir si un trade a été copié

| Où regarder | Ce que cela vous indique |
|---------------|-------------------|
| Copy activity | Ce que le trader a fait |
| Trade history | Les résultats de vos tentatives de copie (exécutée / ignorée / échouée) |
| Positions | Ce que vous détenez actuellement |
| My copies | Statut de la règle : Following / Manually paused / Funding alert |

## 5. Les réseaux de dépôt et de retrait diffèrent (important)

- **Dépôt** : Polygon (PoS) et BSC (lorsqu'il est activé), actifs USDC / USDT
- **Retrait** : **USDC sur Polygon (PoS)** uniquement
- Les deux réseaux de dépôt utilisent des **adresses différentes** — ne les confondez jamais

Voir [Réseaux pris en charge](../wallet/supported-networks.md).

## 6. Le modèle de sécurité en bref

CopyOdds utilise un **compte de trading en garde** : un portefeuille par utilisateur, avec des clés privées isolées. Les retraits nécessitent une vérification renforcée par **Authenticator (TOTP)**. Voir [Sécurité](../security/wallet-security.md).
