# Paramètres de copie

Ce que signifie chaque paramètre de l'assistant de copie. Pour les champs non affichés dans l'assistant (comme certaines limites quotidiennes ou certains délais), fiez-vous à l'interface actuelle de l'App ; les limites avancées décrites dans d'anciennes documentations ont pu être regroupées.

***

## Paramètres de base

| Paramètre | Description |
|---------|-------------|
| **Leader address** | L'adresse de portefeuille à copier ; elle doit être correcte |
| **Name** | Nom d'affichage de la règle, facultatif |
| **Copy mode** | Au choix : **Ratio** (par défaut) / **By balance %** / **Fixed amount** |
| **Copy ratio** | Mode Ratio uniquement : exécution du trader × ratio = le montant de votre ordre |
| **Slippage tolerance** | Écart acceptable par rapport au prix d'exécution du trader ; **15%** par défaut, réglable de 1% à 100% |

### Comment aborder le slippage

Slippage réglé **trop serré** : plus de risques d'ignorance ou d'échec lorsque les prix bougent.  
Slippage réglé **trop large** : plus de chances d'exécution, mais potentiellement à un prix moins favorable.  
La valeur par défaut de 15% vise à améliorer les taux d'exécution ; ajustez-la selon votre propre appétit pour le risque. Le mode Ratio comporte aussi deux paramètres supplémentaires, « Leader order size range » et « Copy ratio » — voir [Les trois modes de copie](copy-modes.md).

***

## Paramètres du mode Ratio

| Paramètre | Description |
|---------|-------------|
| **Copy ratio** | 0.1%–100% ; la page affiche une valeur suggérée avec « environ N trades/jour » |
| **Leader order size range** | Dérivée de la plus grosse exécution historique du trader ; en dessous de la borne basse, l'ordre est ignoré ; au-dessus de la borne haute, il est calculé comme « borne haute × ratio » |

Pour l'explication complète et des exemples, consultez [Les trois modes de copie](copy-modes.md).

***

## Paramètres avancés

| Paramètre | Description |
|---------|-------------|
| **Direction · Both sides** | Copier les achats et les ventes |
| **Direction · Buy only** | Copier uniquement les achats |
| **Direction · Sell only** | Copier uniquement les ventes |
| **Max open copy buys** | Nombre maximal d'achats copiés simultanés pour une même règle ; **1 par défaut = pas de renforcement des positions** ; le maximum affiche **All = illimité** |

### Pourquoi pas de renforcement des positions par défaut ?

Les positions sur un même marché prédictif peuvent s'accumuler rapidement. La valeur par défaut de 1 aide à limiter le risque sur un seul marché ; augmentez-la une fois que vous avez confirmé que la stratégie vous convient.

***

## Comportement par défaut de la plateforme (bon à savoir)

- **Délai de copie** : actuellement, le produit tente généralement l'ordre immédiatement (sans délai artificiel supplémentaire)
- **Pause après des échecs consécutifs** : la plateforme peut brièvement mettre les achats en pause après des échecs répétés (les seuils exacts peuvent varier) ; après avoir corrigé le problème, vous pouvez reprendre dans **My copies**

***

## « Limites souples » liées au financement

Il ne s'agit pas nécessairement de paramètres, mais ils agissent comme des limites :

| Situation | Effet |
|-----------|--------|
| Gas = 0 | Les achats sont ignorés ; achetez du Gas et appuyez sur **Resume buys** (reprendre les achats) |
| USDC insuffisants | Les achats sont ignorés ; déposez davantage ou baissez le montant / pourcentage |
| Moins d'environ $1 | Les achats peuvent ne pas atteindre le notionnel minimum de la plateforme d'échange |

***

## Modifier les paramètres

1. Ouvrez **My copies** (mes copies)
2. Trouvez la règle → **Edit**
3. Après l'enregistrement, seules les exécutions futures sont affectées

Si la simulation est activée dans votre environnement, elle peut exposer davantage de paramètres de type limite ; pour la copie en réel, ce sont les champs de l'assistant qui comptent.

***

## Champs de la page Quick copy

En plus de démarrer une copie depuis le profil d'un trader, vous pouvez aussi coller directement une adresse sur la page **Quick copy** (`/copier`) :

| Champ | Description |
|-------|-------------|
| **Copy ratio** | Suit en pourcentage de votre solde disponible ; 100% utilise la totalité du solde, 5% correspond à une position légère |
| **Per-trade cap (USDC)** | Le maximum que vous engagerez sur un seul trade |
| **Total cap (USDC)** | Le maximum que vous engagerez sur l'ensemble des copies cumulées |
| **Auto-copy toggle** | Lorsqu'il est activé, le système utilise votre portefeuille en garde pour copier automatiquement les ordres de cet utilisateur |

Définir à nouveau la même adresse **écrase** la règle précédente ; après des modifications, vérifiez une fois dans **My copies**.
