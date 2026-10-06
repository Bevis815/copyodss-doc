# FAQ

En cas de problème, consultez d'abord cette page. Si vous ne parvenez toujours pas à le résoudre, veuillez préparer : votre e-mail d'inscription, l'heure de l'action, des captures d'écran de l'erreur et le hash de la transaction ou l'ID de l'historique des trades.

---

## Compte et connexion

### Les nouveaux utilisateurs doivent-ils s'inscrire séparément ?

Dans la plupart des cas, saisir une **nouvelle adresse e-mail** sur la page de connexion et valider le code crée automatiquement un compte. Si l'écran vous demande encore un nom / l'acceptation des conditions, suivez simplement les instructions.

### Vous ne recevez pas le code de vérification ?

Vérifiez votre dossier de spam et l'orthographe de l'adresse e-mail ; renvoyez le code une fois le compte à rebours terminé. Les serveurs de messagerie d'entreprise le bloquent parfois — essayez une adresse e-mail personnelle que vous utilisez souvent.

### Que faire si la Passkey échoue ?

Connectez-vous plutôt avec un code par e-mail ; assurez-vous que votre navigateur est pris en charge et que vous n'utilisez pas une WebView intégrée incompatible, puis ajoutez à nouveau la Passkey dans les paramètres.

---

## Configuration du compte et autorisation

### Dois-je demander l'ouverture d'un compte de trading ?

**Non.** Il est généralement ouvert automatiquement après la connexion, vous pouvez donc déposer immédiatement. Dans le cas rare où il indique « pas encore ouvert », appuyez pour l'ouvrir et acceptez le contrat. Voir [Compte de trading et statut de la page Portefeuille](wallet/trading-account.md).

### La page Portefeuille affiche « Agent authorization » — dois-je payer du gas ?

Non. La signature est gratuite et la plateforme prend en charge les frais on-chain. Il vous suffit d'utiliser le portefeuille avec lequel vous vous êtes inscrit, basculé sur **Polygon (chain ID 137)**.

### « Polymarket trading authorization incomplete » est-il un problème ?

Appuyez simplement sur **Re-authorize Polymarket**. Il s'agit d'un problème à l'étape d'autorisation, qui **n'affecte pas les fonds que vous avez déjà déposés**.

### Pourquoi y a-t-il deux montants, « solde on-chain » et « solde disponible » ?

Le solde on-chain correspond aux USDC natifs effectivement arrivés ; le solde disponible est la partie traitée et prête pour la copie. Ils peuvent différer pendant quelques minutes juste après un dépôt — c'est normal.

---

## Dépôts et solde

### Pourquoi mon solde n'a-t-il pas été mis à jour après mon dépôt ?

Vérifiez que : le réseau est **Polygon ou BSC (celui de la page)**, l'actif est de l'**USDC/USDT**, l'adresse correspond exactement à celle de cette page, et la transaction est confirmée on-chain. BSC peut être plus lent. Actualisez votre solde après confirmation ; s'il n'est toujours pas arrivé, fournissez le hash de la transaction.

### Puis-je déposer des USDT ?

Oui, mais il doit s'agir d'USDT sur le réseau sélectionné sur la page, envoyés uniquement à l'adresse de cette page. Ne forcez pas un retrait depuis le mauvais réseau.

### Que se passe-t-il si le portefeuille de destination n'a pas de MATIC ?

Le retrait réussira, mais **vous ne pourrez pas déplacer ces USDC on-chain par la suite**. Conservez un peu de MATIC (POL) sur l'adresse de réception.

### Le retrait indique « channel busy » — que dois-je faire ?

Attendez quelques minutes ou quelques heures comme indiqué, puis réessayez. **Vos fonds sont en sécurité** et vous n'avez pas besoin de soumettre à nouveau la demande.

### Juste après l'arrivée des fonds, il est indiqué « conversion automatique en solde négociable » ?

C'est normal. Les USDC natifs arrivés on-chain doivent être convertis automatiquement en solde négociable — attendez quelques minutes et actualisez.

### Puis-je confirmer un retrait avec une Passkey ou un code par e-mail ?

**Non.** Les retraits n'acceptent actuellement que les **codes Authenticator** ; les Passkeys et les codes par e-mail servent uniquement à la connexion et à des scénarios similaires.

### La désactivation de l'Authenticator nécessite-t-elle un code ?

Oui. Pour des raisons de sécurité, la désactivation nécessite également un code à 6 chiffres. Si vous changez d'appareil, il est plus simple de le réassocier directement sur le nouvel appareil.

### Pourquoi le montant retirable est-il inférieur à mon solde ?

Les positions et les ordres ouverts immobilisent des fonds. Fiez-vous au **Max withdrawable** (montant maximal retirable).

### Les adresses Polygon et BSC sont-elles les mêmes ?

**Non.** Ne les confondez jamais. Voir [Réseaux pris en charge](wallet/supported-networks.md).

---

## Gas et copie

### Quelle est la différence entre le Gas de la plateforme et les MATIC / BNB ?

Le Gas de la plateforme est un crédit de frais de service CopyOdds acheté avec des USDC dans le Gas Store. Les MATIC / BNB sont des jetons natifs on-chain utilisés pour les frais de réseau — **ce n'est pas la même chose**.

### Pourquoi ne puis-je pas ajouter ou reprendre une règle de copie ?

La raison la plus courante est **Gas = 0**. Achetez du Gas, puis activez / reprenez la règle.

### De combien d'USDC ai-je besoin pour commencer à copier ?

L'activation d'une règle nécessite généralement seulement Gas > 0. Mais chaque achat effectif nécessite environ **$1** ou plus d'USDC disponibles.

### J'ai acheté du Gas / déposé des fonds — pourquoi toujours aucun achat copié ?

Lorsque les fonds sont insuffisants, les achats sont ignorés mais la règle n'est pas forcément mise en pause. Après avoir rechargé, allez dans **My copies** (mes copies) et appuyez sur **Resume buys** (reprendre les achats). Vérifiez également dans Trade history les échecs dus au slippage, les incompatibilités de direction ou l'atteinte de la limite d'interdiction de renforcer les positions.

---

## Exécution des copies

### Pourquoi certains trades n'ont-ils pas été copiés ?

Raisons courantes : paramètres de direction, montant trop faible, limite d'interdiction de renforcer les positions, slippage, USDC/Gas insuffisants, aucune part à vendre, liquidité insuffisante. Ouvrez Trade history pour voir le statut précis.

### Copy activity indique que le trader a acheté — pourquoi pas moi ?

Copy activity ≠ vos exécutions. Consultez Trade history.

### Le trader a vendu — pourquoi pas moi ?

Vous devez détenir des parts sur ce marché. Si vous n'avez jamais acheté ou si vous avez déjà tout vendu, une vente ignorée est normale.

### Quelle est la différence entre mettre en pause et supprimer ?

Une règle en pause peut être reprise ; une règle supprimée doit être recréée. Aucune des deux ne clôture automatiquement vos positions.

---

## Retraits et sécurité

### Pourquoi les retraits nécessitent-ils une vérification renforcée ?

Pour protéger vos fonds et empêcher que des actifs soient transférés directement si une session est détournée. Les retraits n'acceptent actuellement que les codes **Authenticator** ; si vous n'en avez pas configuré, activez-le d'abord dans les paramètres. Les Passkeys et les codes par e-mail ne peuvent pas être utilisés pour les retraits.

### Une Passkey peut-elle être utilisée pour retirer ?

Non. Une Passkey est un raccourci pour la **connexion** ; les retraits n'acceptent que les codes Authenticator.

### Impossible de retirer après m'être connecté sur un nouveau téléphone ?

Un délai de carence pour nouvel appareil a peut-être été déclenché, ou l'Authenticator n'est pas encore configuré dans le nouvel environnement. Réessayez plus tard et vérifiez la gestion des appareils et votre association TOTP ; contactez le support si l'échec persiste.

### L'équipe officielle me demandera-t-elle un jour ma phrase de récupération ?

**Jamais.** Voir [Anti-hameçonnage](security/anti-phishing.md).

---

## Smart money

### Le classement garantit-il des profits ?

**Non.** Les indicateurs reposent sur des données publiques et des modèles, et incluent des hypothèses de simulation ; les performances passées ≠ les rendements futurs.

### Comment ouvrir le profil d'un trader ?

`https://app.copyodds.io/@0xADDRESS` (ajoutez `/zh` pour l'interface chinoise).

### « Copy fit / backtest P&L » correspondent-ils à mes rendements réels ?

Non. Il s'agit principalement de simulations supposant un délai + du slippage ; vos résultats réels se trouvent dans Trade history.

---

## Modes de copie

### Quels sont les modes de copie et lequel choisir ?

**Ratio** (par défaut), **By balance %** (en % du solde) et **Fixed amount** (montant fixe). Si c'est votre première fois, utilisez simplement le mode par défaut **Ratio** : vous achetez un pourcentage de chaque achat du trader, ce qui rend très difficile qu'un de ses gros paris fasse exploser votre compte. Voir [Les trois modes de copie](copy-trading/copy-modes.md).

### Que signifie « Ratio » ?

Si le trader achète pour $5,000 en un trade et que votre ratio est de 10%, vous achetez pour $500. La plage du ratio va de 0.1% à 100%.

### À quoi sert la « Leader order size range » (plage de taille des ordres du trader) en mode Ratio ?

Elle filtre les ordres poussière minuscules et les ordres surdimensionnés. Les ordres inférieurs à la borne basse sont ignorés ; les ordres supérieurs à la borne haute sont toujours copiés, mais le montant est calculé comme « borne haute × ratio », de sorte qu'un gros pari du trader ne soit pas amplifié.

### Puis-je simplement utiliser le « Suggested ratio » (ratio suggéré) proposé par la page ?

Oui. Il est calculé comme « votre solde disponible ÷ (borne haute de la plage × nombre approximatif de trades par jour du trader) », conçu pour que **vous utilisiez environ ce nombre de trades sur une journée**. Baissez-le manuellement si vous voulez être plus prudent.

### Pourquoi mon trade a-t-il été ignoré avec « Outside size band » ?

L'ordre du trader était trop petit (inférieur à la borne basse de la plage). Il s'agit d'un ordre poussière filtré volontairement, pas d'un bug.

### Que se passe-t-il si le montant calculé est inférieur à $1 ?

Tant que votre solde est suffisant, le système **le complète automatiquement à $1** (le minimum d'achat de la plateforme d'échange) et passe l'ordre au lieu de l'ignorer.

### Le slippage par défaut est-il de 30% ou de 15% ?

La valeur par défaut dans les paramètres de copie est de **15%**, réglable de 1% à 100%.

### Pourquoi les paramètres sont-ils pré-remplis lorsque je copie depuis le profil d'un trader ?

Le système utilise les résultats de la « simulation de copie » pour pré-remplir le slippage et le nombre maximal d'achats copiés ; la page indiquera « Pre-filled from copy simulation ».

---

## Nouvelles fonctionnalités

### Quelle est la différence entre Leaderboard et Smart money ?

Leaderboard affiche le **classement des profits quotidiens des comptes du pool de copie** (page d'accueil) ; Smart money affiche le **score et le profil des adresses de traders individuels**. Pour choisir des traders, utilisez d'abord le Leaderboard pour trouver une orientation, puis affinez avec les filtres de Smart money.

### « Copy activity » et « Trade history » sont-ils la même chose ?

Non. Copy activity montre **ce que le trader a fait** ; Trade history montre **les résultats de vos tentatives de copie**. Comparer les deux est le moyen le plus simple de repérer les problèmes.

### Le copy trading en simulation utilise-t-il mon argent réel ?

**Non.** Le copy trading en simulation fonctionne dans un compte virtuel distinct et ne nécessite pas non plus de Gas.

### Pourquoi ne puis-je pas vendre ma position ?

Elle est peut-être « en attente de règlement » (le marché est terminé et attend d'être réglé), ou il n'y a peut-être aucun ordre d'achat sur ce marché pour le moment. Si vous avez gagné, un bouton **Redeem** (récupérer) apparaîtra.

### « Transaction history » sur la page Portefeuille est-il identique au menu de l'historique des trades ?

Non. **Executions** dans le menu correspond à votre **historique des trades copiés** ; **Transaction history (`/wallets/ledger`)** dans le portefeuille est votre **registre des mouvements de fonds et des dépenses de Gas**.

### La suppression d'un appareil dans la gestion des appareils affectera-t-elle mes copies ?

Elle ne supprimera pas vos règles de copie, mais les sessions de connexion de l'ancien appareil sont immédiatement invalidées et il devra se reconnecter.

### La commission sur la page d'affiliation est-elle toujours de 10% ?

Non. Votre taux de commission dépend de votre **niveau** (de L1 à 10% jusqu'au niveau le plus élevé). Le niveau L1 est activé automatiquement après un achat, puis vous montez automatiquement de niveau en fonction de votre nombre de filleuls directs ; le niveau le plus élevé doit être acheté.

### Dois-je télécharger l'App sur mon téléphone ?

Non. La version web est complète ; pour une expérience plus proche d'une application, utilisez la fonction « Ajouter à l'écran d'accueil » de votre navigateur. Voir [Utiliser CopyOdds sur mobile](getting-started/mobile-app.md).

---

## Avertissement sur les risques

- Les prix du marché fluctuent et le copy trading peut entraîner des pertes
- La copie automatisée peut s'écarter du trader en raison du slippage, du délai et de la liquidité
- Une mauvaise chaîne, une mauvaise adresse ou un mauvais jeton peut entraîner la non-réception ou la perte irrécupérable des fonds
- Un solde de Gas / d'USDC insuffisant fait que les achats sont ignorés
- Les résultats du classement et des simulations sont fournis à titre indicatif uniquement et ne constituent pas une promesse de rendement

Les nouveaux utilisateurs devraient d'abord parcourir l'ensemble du processus avec un petit montant : Déposer → Acheter du Gas → Copier → Vérifier Trade history → Puis essayer un petit retrait.
