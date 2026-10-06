# Copy trading en simulation

Le **copy trading en simulation** exécute votre stratégie de copie avec un « portefeuille virtuel » — **sans argent réel**, uniquement pour tester des paramètres et observer les résultats. C'est idéal pour les débutants qui ne sont pas encore prêts à engager de l'argent réel.

Accès : **Simulation copy trading** → `/copy-trading/simulation`

> Le copy trading en simulation est déployé progressivement. Si vous ne voyez pas ce menu, il n'a pas encore été activé pour vous.

***

## En quoi il diffère de la copie en réel

| | Simulation | Copie en réel |
|--|------------|--------------|
| Argent | Solde virtuel | Vos USDC en garde |
| Gas | Non nécessaire | Nécessaire (environ 0.5% de frais de service par trade) |
| Pouvez-vous perdre de l'argent ? | Pas réellement | Oui |
| Objectif | Tester des paramètres, observer les performances à long terme | Rendements réels |

***

## Démarrer en trois étapes

### 1. Créer un compte virtuel

Appuyez sur **Create virtual account** (créer un compte virtuel) et renseignez :

| Champ | Description |
|-------|-------------|
| Nom du compte | Un nom pour les distinguer, par ex. « Test-A » |
| Solde de départ | Capital simulé |
| Durée (jours) | Après expiration, aucune nouvelle position n'est ouverte ; les positions existantes peuvent toujours être clôturées ou réglées |

### 2. Ajouter des adresses à copier

Ajoutez des adresses de traders sous **Copy addresses** ; vous pouvez nommer la stratégie et ajouter des notes.

### 3. Configurer la stratégie

| Paramètre | Description |
|---------|-------------|
| Méthode de copie | Ratio / Fixed amount |
| Direction | Achat et vente / Achat uniquement / Vente uniquement |
| Min / Max par trade | Plage de montant pour chaque trade |
| Plafond par marché | Le maximum à engager sur un seul marché |
| Plafond quotidien | Le maximum à engager par jour |
| Slippage maximal | Pas d'exécution en cas de dépassement |
| Délai d'exécution | Simule une « réaction un peu plus lente » |
| Temps de recharge par marché | Intervalle minimal entre deux copies sur le même marché |
| Pause après des échecs consécutifs | Mise en pause après ce nombre d'échecs d'affilée (10 par défaut) |

Appuyez sur **Start simulation copy** (lancer la copie en simulation) pour l'exécuter.

***

## Consulter les résultats : cinq onglets

| Onglet | Contenu |
|-----|---------|
| **Copy addresses** | Les adresses que vous avez ajoutées, les paramètres de stratégie et le statut |
| **Positions** | Positions simulées ; vous pouvez simuler leur clôture manuellement |
| **Executions** | Parts, frais et statut de chaque exécution simulée |
| **Performance** | Courbe du capital, P&L total, taux de réussite, drawdown maximal, coût du slippage, coût des frais, etc. |
| **Ledger** | Détail de chaque mouvement de fonds |

### Statuts

| Statut du compte | Signification |
|----------------|---------|
| Active | Fonctionnement normal |
| Paused | Vous l'avez mis en pause ; il peut être repris |
| Expired | Aucune nouvelle position ; le capital existant peut toujours être géré |
| Archived | Rangé ; ne peut pas être archivé tant qu'il détient des positions |

### Remarque sur la clôture des positions

La clôture manuelle nécessite un **prix de marché datant de moins de 15 minutes** pour obtenir une cotation ; si le prix est obsolète ou manquant, il vous sera demandé d'actualiser la cotation. Avant de confirmer, vous verrez le prix d'exécution estimé, le slippage, les frais, le produit estimé et le P&L estimé.

***

## En une phrase

La véritable valeur du copy trading en simulation est la suivante : **avant de dépenser de l'argent réel, vous pouvez voir à quoi mènent réellement « copie fréquente + slippage élevé + petit capital ».**
