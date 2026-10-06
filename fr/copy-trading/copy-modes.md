# Les trois modes de copie (les débutants commencent ici)

La première chose à choisir dans les paramètres de copie est le **mode de copie**. Il en existe actuellement trois :

| Mode | Résumé en une ligne | Idéal pour |
|------|------------------|----------|
| **Ratio** (nouveau, par défaut) | Vous achetez un **pourcentage fixe** de chaque achat du trader | La plupart des gens, surtout lorsque la taille des ordres du trader varie beaucoup |
| **By balance %** (en % du solde) | Chaque trade utilise un **pourcentage de votre propre solde** | Ceux qui veulent que la taille des positions suive automatiquement leur solde |
| **Fixed amount** (montant fixe) | Chaque trade achète **le même montant** | Les traders dont la taille des ordres est assez constante |

> **Les nouveaux utilisateurs sont par défaut en mode Ratio.** C'est actuellement le mode le plus recommandé, et il est détaillé plus en profondeur ci-dessous.

***

## Pourquoi le mode Ratio a-t-il été ajouté ?

Le montant fixe pose un problème courant : le trader achète pour $30 une fois et pour $3,000 la suivante, mais vous copiez toujours $10 — vous manquez donc complètement son rythme, soit en copiant trop peu pour que cela compte, soit en copiant aveuglément trop.

Le mode Ratio change cela en : **quel que soit le montant qu'il place, vous placez un montant proportionnel**.

| Exécution du trader | Votre mode Fixed amount | Votre mode Ratio (10%) |
|---------------|------------------------|-----------------------|
| $50 | Copie $10 | Copie $5 |
| $500 | Copie $10 | Copie $50 |
| $5,000 | Copie $10 | Copie $500 |

L'avantage est qu'il **suit naturellement le dimensionnement des positions du trader**, sans qu'un gros pari occasionnel de sa part ne fasse exploser votre compte.

***

## Le mode Ratio en détail

### Trois éléments à régler

| Paramètre | Emplacement | Description |
|---------|-------|-------------|
| **Copy ratio** (ratio de copie) | Curseur sous le mode | 0.1%–100%. Exécution du trader × ce ratio = le montant de votre ordre |
| **Leader order size range** (plage de taille des ordres du trader) | Second curseur sous le mode | Ne copie que les ordres de « taille normale » du trader, en filtrant les ordres poussière et surdimensionnés |
| **Slippage tolerance** (tolérance au slippage) | Sous le mode | 1%–100%, **15%** par défaut |

### 1. Ratio de copie

C'est le ratio qui définit « combien copier ». La page des paramètres affiche une ligne d'aperçu :

> Le trader place 100, vous réglez 10%, donc le vôtre est de 10.

La page affiche généralement aussi un **Suggested ratio** (ratio suggéré) à côté de « environ N trades/jour ». Il est calculé ainsi :

> **Ratio suggéré ≈ votre solde disponible ÷ (borne haute de la plage × nombre approximatif de trades par jour du trader)**

Exemple : vous disposez de $1,000, le trader achète environ 5 fois par jour et la borne haute de la plage est de $800.
Ratio suggéré ≈ 1000 ÷ (800 × 5) = 25%. Autrement dit, **vous utiliserez l'équivalent d'environ 5 trades sur une journée**, et un gros ordre ne videra pas votre solde d'un coup.

Si vous ne voulez pas de la valeur suggérée, faites simplement glisser le curseur pour définir la vôtre, de 0.1% à 100%.

> Astuce : une fois que vous avez déplacé le curseur, le système cesse de remplacer automatiquement votre choix ; la suggestion n'est recalculée que lorsque vous actualisez ou choisissez à nouveau un trader.

### 2. Plage de taille des ordres du trader

Cette plage est dérivée de **la plus grosse exécution unique historique du trader**, et correspond par défaut à la partie centrale (environ 5%–95%). Elle filtre deux types d'ordres :

| Situation | Traitement | Pourquoi |
|-----------|----------|-----|
| Le trader achète **trop peu** (sous la borne basse) | **Ignoré**, non copié | Ces « ordres poussière » ne valent pas la peine d'être copiés et ne feraient que coûter du Gas |
| Le trader achète **dans la plage** | Copié normalement selon votre ratio | C'est l'activité habituelle du trader |
| Le trader achète **trop** (au-dessus de la borne haute) | **Toujours copié**, mais le montant est calculé comme « borne haute × votre ratio » | Évite qu'un gros pari occasionnel n'engage tout votre argent |

La page propose des préréglages prêts à l'emploi :

| Préréglage | Signification | Idéal pour |
|--------|---------|----------|
| **All 0–100%** | Aucun filtrage | Les traders dont la taille des ordres est très régulière |
| **Balanced 1–99%** | Copie presque tout, en filtrant uniquement les extrêmes | **Par défaut, idéal pour les débutants** |
| **Core 20–80%** | Ne copie que la partie centrale principale | Plus prudent, ne copie que l'activité principale |

**Exemple officiel** : plage $200–$800, ratio 10%, le trader achète pour $5,000 → vous ne copiez que $80.

> Astuce : juste après avoir choisi un trader, s'il n'existe pas encore de données d'exécution historiques le concernant, la page indiquera « No cache yet; copying at the default ratio for now, actual amounts will be capped by your balance » (pas encore de cache ; copie au ratio par défaut pour l'instant, les montants réels seront plafonnés par votre solde) — c'est normal.

### 3. Tolérance au slippage

- Signification : l'écart maximal autorisé sur le prix d'exécution
- **15%** par défaut, réglable de 1% à 100%
- **Plus serrée** : plus de risques d'ignorance ou d'échec lorsque les prix bougent
- **Plus large** : plus de chances d'exécution, mais potentiellement à un prix moins favorable

> Lorsque vous commencez à copier depuis le profil d'un trader, le système utilise les résultats de la « simulation de copie » pour pré-remplir le slippage et le nombre maximal d'achats copiés ; la page indiquera « Pre-filled from copy simulation ».

***

## Comment un trade copié est réellement calculé

Supposons que vous ayez réglé : ratio **10%**, plage **$200–$800**, solde $1,000.

| Étape | Description |
|------|-------------|
| 1. Regarder l'exécution du trader | Il a acheté pour $5,000 |
| 2. Vérifier si elle est dans la plage | Au-dessus de la borne haute de $800, donc **non ignorée**, mais calculée à partir de la borne haute |
| 3. Calculer le montant | Prendre le **plus petit** entre « exécution du trader × 10% » et « borne haute × 10% » = $80 |
| 4. Vérifier votre solde | Continuer si le solde ≥ $1 ; s'il est insuffisant, passer l'ordre avec ce que votre solde permet réellement |
| 5. Compléter jusqu'au minimum | Si le résultat est inférieur à $1, il est **complété à $1** (le minimum d'achat de la plateforme d'échange) tant que votre solde le permet |
| 6. Déduire le Gas | Après l'exécution, environ 0.5% est déduit en Gas de la plateforme |

Voici maintenant un cas dans la plage : le trader achète pour $500 → 500 × 10% = $50, copié normalement pour $50.

***

## Quand les trades sont ignorés

| Message dans l'App | En termes simples | Que faire |
|--------------------|----------------|------------|
| **Outside size band** | L'ordre du trader était trop petit — un ordre poussière | Rien ; c'est voulu |
| **Insufficient funds** | Votre solde disponible est inférieur à $1 | Déposez des fonds ou baissez le ratio |
| **Your size < $1** | Trop petit même après complément | Augmentez le ratio ou baissez la borne haute de la plage |
| **Price ≥ $0.85** | Le trader a acheté une issue déjà cotée comme « quasi certaine » | Rien |
| **Already open (no add-on)** | Vous avez déjà copié une entrée sur ce marché | Conservez le réglage par défaut « pas de renforcement » ou modifiez le paramètre |
| **Slippage too high** | Le prix s'est éloigné | Envisagez d'assouplir le slippage |
| **Low Gas** | Vous n'avez plus de Gas de la plateforme | Rechargez dans le [Gas Store](../wallet/gas.md) |

> Remarque : la règle **« moins de $1 est complété à $1 »** s'applique aux trois modes (Ratio, Fixed amount, By balance %). Les ordres inférieurs à $1 ne sont donc pas ignorés — ils sont complétés et copiés (tant que votre solde le permet).

***

## Les deux autres modes

### By balance %

- Chaque trade utilise un **pourcentage de votre propre solde USDC disponible** ; par ex. à 5% avec un solde de $1,000, chaque trade achète pour $50
- À mesure que votre solde augmente, chaque trade augmente automatiquement ; lorsqu'il diminue, les trades diminuent
- Les résultats inférieurs à $1 sont également complétés à $1

**Idéal pour** : ceux qui veulent que la taille des positions suive leur solde sans ajuster constamment les montants à la main.

### Fixed amount

- Chaque trade achète **le même montant**, par ex. $25 à chaque fois
- Minimum $1
- Règle spéciale pour les petits ordres : lorsque le montant est inférieur à $1, s'il représente **≥ 5 parts**, l'ordre utilise le montant défini ; s'il représente **moins de 5 parts**, il est automatiquement ajusté à $1

**Idéal pour** : les traders dont la taille des ordres est assez constante (par ex. environ $200 par trade sur le long terme), lorsque vous voulez contrôler précisément le coût de chaque trade.

***

## Lequel choisir ?

| Votre situation | Recommandation |
|----------------|----------------|
| Première fois, vous ne savez pas quoi choisir | **Ratio** (par défaut) |
| La taille des ordres du trader varie beaucoup | **Ratio** |
| Vous voulez contrôler précisément le montant de chaque trade | **Fixed amount** |
| Vous voulez que la taille des positions suive votre solde | **By balance %** |

***

## FAQ

**Quel est le montant maximal qui peut être engagé par trade en mode Ratio ?**

Il n'y a pas de plafond distinct par trade — votre ratio × l'exécution du trader donne le montant, mais celui-ci est limité à la fois par la « borne haute de la plage » et par « votre solde ». Pour être plus prudent, baissez le ratio et la borne haute de la plage.

**J'hésite à utiliser directement le ratio suggéré.**

Vous pouvez l'utiliser directement ; le système tient déjà compte du « nombre approximatif de trades par jour ». Pour plus de sécurité, commencez une petite règle avec un ratio plus faible, observez pendant un jour ou deux s'il y a beaucoup d'ignorances, puis augmentez progressivement.

**Le mode Ratio entre-t-il en conflit avec « pas de renforcement des positions » ?**

Non. Le réglage par défaut « 1 achat copié maximum » (pas de renforcement) signifie que **le même marché** n'est acheté qu'une seule fois ; le ratio contrôle **combien ce trade achète**. Pour renforcer les positions, augmentez « Max open copy buys » dans les paramètres avancés — **le maximum est All (illimité)**.

**Le slippage par défaut dans les paramètres est-il de 30% ou de 15% ?**

Il est désormais de **15%**, réglable de 1% à 100%.

**Existe-t-il aussi un « guide du Ratio » officiel dans l'App ?**

Oui. Appuyez sur **Ratio guide** en haut à droite du mode Ratio (ou sur la page des paramètres) pour l'ouvrir. C'est la version détaillée propre à la plateforme ; cette page en est l'explication complète pour les débutants.

***

## Pages associées

- Suivez-le étape par étape : [Comment copier un trader](how-to-follow.md)
- Ce que signifie chaque paramètre : [Paramètres de copie](settings.md)
- Comment gérer après l'activation : [Gérer vos copies](managing.md)
- Essayez d'abord sans dépenser d'argent : [Copy trading en simulation](simulation.md)
