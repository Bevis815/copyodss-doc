# Comment copier un trader

Ajoutez une adresse smart money à la copie automatisée et enregistrez la règle.

![Assistant de copie](../.gitbook/assets/follow_doc.png)

***

## Liste de vérification préalable

| Condition | Remarques |
|-----------|-------|
| Connecté avec un compte de trading actif | Généralement ouvert automatiquement après la connexion |
| Gas de la plateforme > 0 | **Obligatoire** ; sinon vous ne pouvez pas activer / reprendre |
| Solde USDC disponible | Environ $1 ou plus recommandé ; sinon les achats risquent d'être ignorés |

***

## Points d'entrée

Au choix :

1. Appuyez sur **Follow** (suivre) dans la liste **Smart money** ou sur une page de profil
2. **Quick copy / New copy** (copie rapide / nouvelle copie) dans **My copies** (mes copies)
3. Ouvrez directement `/copier` (Quick copy) et collez une adresse
4. Ouvrez un lien de profil `https://app.copyodds.io/@0x...` et appuyez sur Follow

***

## Étapes

1. Vérifiez la **Leader address** (adresse du trader suivi) (0x…) ; la reprendre depuis le classement évite les fautes de frappe
2. Facultatif : nommez la règle (Name this copy trade)
3. Choisissez un **Copy mode** (mode de copie) — choisissez-en un parmi trois :
   - **Ratio** — **Le mode par défaut** ; copie un pourcentage fixe de chaque exécution du trader (le trader achète pour $500 avec un ratio de 10% → vous achetez pour $50)
   - **By balance %** — Un pourcentage de **vos USDC disponibles** (1%–100%)
   - **Fixed amount** — Achète le même montant à chaque fois (minimum $1)
4. Réglez la **Slippage tolerance** (tolérance au slippage) — **15%** par défaut, réglable de 1% à 100%

   > Pour savoir en quoi les trois modes diffèrent, comment le ratio est calculé et d'où viennent les valeurs suggérées, consultez [Les trois modes de copie](copy-modes.md)
5. Ouvrez éventuellement les **Advanced settings** (paramètres avancés) :
   - **Direction** : Both / Buy only / Sell only
   - **Max open copy buys** : **1** par défaut (pas de renforcement des positions) ; le maximum est **All (illimité)**
6. Enregistrez (**Copy trade / Save**)
7. Allez dans **My copies** et vérifiez que le statut est **Following** (suivi en cours)

***

## Montant fixe vs % du solde

| Mode | Comportement | Idéal pour |
|------|----------|----------|
| Montant fixe | Que le trader achète pour $50 ou $500, vous copiez avec le montant défini | Maîtriser le risque par trade |
| % du solde | Copie les achats avec un % de votre solde disponible à ce moment-là | S'adapter automatiquement à votre capital |

Si le montant calculé à partir du pourcentage est inférieur à la taille minimale d'ordre, le système peut le relever au minimum avant de tenter l'ordre.

***

## Remarques

- Chaque adresse de trader suivi n'a généralement qu'un seul ensemble de paramètres actif ; enregistrer à nouveau l'écrase
- La modification d'une règle n'affecte que les copies futures et ne réécrit pas les exécutions passées
- Arrêter / supprimer une règle **ne vend pas** automatiquement vos positions
- Testez d'abord avec un petit montant, et n'augmentez qu'une fois que Trade history semble normal

***

## Où regarder après la copie

| Ce que vous voulez voir | Où aller |
|----------------------|-------------|
| Ce que le trader vient de faire, et si je l'ai copié | [Activité de copie](copy-activity.md) |
| Ce que je détiens actuellement | [Mes positions et historique des trades](positions-and-records.md) |
| Statut de la règle, pause / reprise | [Gérer vos copies](managing.md) |
