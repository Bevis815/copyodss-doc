# Compte de trading et statut de la page Portefeuille

Votre **compte de trading CopyOdds est généralement ouvert automatiquement après la connexion** — aucune demande séparée n'est nécessaire. Il s'agit de votre **portefeuille de trading en garde** : les USDC / USDT que vous déposez y sont conservés et servent au copy trading.

Accès : **Wallets** → `/wallets` (l'élément de menu **Deposit** ouvre cette page)

***

## Ce que vous verrez normalement

| Section | Contenu |
|---------|---------|
| Adresse de dépôt on-chain | Votre adresse de dépôt (**différente selon le réseau**) ; copiez-la ou enregistrez le QR code |
| Solde disponible | La partie que vous pouvez utiliser immédiatement pour la copie |
| Solde on-chain | Les USDC natifs effectivement arrivés sur la blockchain |
| Gas de la plateforme | Utilisé pour payer les frais de service du copy trading |
| Retrait | Saisissez une adresse de réception Polygon et un montant |
| Historique des transactions | Dépôts, retraits et dépenses de Gas |

Si vous voyez tout cela, tout fonctionne et vous pouvez déposer immédiatement.

***

## Pourquoi les deux soldes diffèrent

| Terme | Signification |
|------|---------|
| **Solde on-chain** | Les USDC natifs effectivement arrivés sur la blockchain |
| **Solde négociable** | La partie que la plateforme a traitée et qui peut être utilisée pour la copie |

Si, juste après un dépôt, vous voyez « xx USDC natifs on-chain, conversion automatique en solde négociable », c'est **le processus normal** — attendez quelques minutes et actualisez.

***

## Statuts que vous pourriez voir occasionnellement

Tout le monde ne les verra pas ; si c'est votre cas, traitez-les comme décrit ci-dessous.

### « Compte de trading CopyOdds pas encore ouvert »

Dans de rares cas, le compte n'est pas ouvert automatiquement (par ex. un problème est survenu pendant la configuration). Appuyez sur **Open trading account** (ouvrir le compte de trading), lisez et cochez le contrat, puis confirmez.

Résumé du contrat :

| Clause | Contenu |
|--------|---------|
| Service | La plateforme crée pour vous un portefeuille de trading en garde, utilisé pour les dépôts, la copie, les ordres et les retraits |
| Garde et autorisation | Les actifs sont détenus par la plateforme et vous ne détenez pas directement la clé privée ; vous autorisez la plateforme à effectuer les signatures et l'exécution des trades nécessaires |
| Protection des retraits | Il peut vous être demandé d'activer la vérification renforcée par **Authenticator (TOTP)** avant de retirer |
| Fonds et réseaux | N'envoyez que des actifs pris en charge à l'adresse et sur le réseau indiqués sur la page ; **choisir le mauvais réseau ou le mauvais actif peut rendre les fonds irrécupérables** |
| Avertissement sur les risques | Le copy trading est **à haut risque et vous pouvez perdre la totalité de votre investissement** ; le slippage, la liquidité et le délai affectent tous les résultats |
| Éligibilité et conformité | Vous devez avoir au moins 18 ans ; le service ne peut pas être utilisé à des fins de blanchiment d'argent, de fraude ou à d'autres fins illégales |

> Le contrat peut être mis à jour ; les conditions complètes figurent dans la fenêtre de l'App et dans les Conditions d'utilisation.

### Une section « Agent authorization » apparaît

Certains comptes voient une section supplémentaire **Agent authorization** (autorisation d'agent) sur la page Portefeuille. Elle vous permet de **donner votre autorisation en une seule signature**, après quoi la plateforme passe les ordres pour vous et **prend en charge le gas on-chain** (vous n'avez pas besoin de vos propres MATIC).

Si vous voyez cette section, suivez simplement les instructions :

| Exigence | Description |
|-------------|-------------|
| Signer avec **le portefeuille avec lequel vous vous êtes inscrit** | Choisir le mauvais compte dans votre portefeuille affiche « Current wallet is not the registered wallet » |
| Basculer votre portefeuille sur **Polygon (chain ID 137)** | Sinon, vous verrez « Please switch your wallet to Polygon and try again » |
| Effectuer la signature en une seule fois | Fermer l'extension ou modifier le contenu en cours de route provoque un échec ; actualisez et recommencez |
| Surveiller l'expiration | Après expiration, la copie se met en pause — appuyez sur **Renew** (renouveler) ; vous pouvez aussi la **Revoke** (révoquer) (vous devrez de nouveau donner votre autorisation après la révocation) |

Erreurs courantes : mauvais portefeuille / mauvaise chaîne / demande d'autorisation expirée / contenu signé ne correspondant pas à la vérification (généralement une interférence d'extension — actualisez et réessayez).

### « Polymarket trading authorization incomplete »

Appuyez sur **Re-authorize Polymarket**. Ce message indique un problème à l'étape d'autorisation et **n'affecte pas les fonds que vous avez déjà déposés**.

> Dans les rares cas où l'autorisation automatique échoue, la page propose une option « Manually paste Polymarket API credentials (advanced) » (coller manuellement les identifiants API Polymarket, avancé) pour le dépannage. Les utilisateurs ordinaires n'ont pas besoin d'y toucher.

***

## FAQ

**Le compte de trading est-il payant ?**  
Son ouverture est gratuite. Environ 0.5% de Gas de la plateforme est déduit uniquement lorsque des trades copiés sont exécutés.

**Où se trouve ma clé privée ?**  
Pas chez vous. CopyOdds utilise un portefeuille en garde dont les clés privées sont stockées de manière isolée par la plateforme ; vous contrôlez vos fonds via la connexion + la vérification renforcée des retraits.

**Pourquoi puis-je voir l'adresse on-chain sans pouvoir transférer les fonds moi-même ?**  
C'est le principe de la garde : l'adresse appartient à la plateforme et sert à recevoir vos dépôts. Pour transférer des fonds, vous devez passer par le processus de **retrait** et effectuer la vérification renforcée.

**Quand les deux soldes diffèrent-ils ?**  
Généralement uniquement pendant les quelques minutes **qui suivent un dépôt, le temps de la conversion automatique**. S'ils restent différents longtemps, actualisez ; si l'écart persiste, contactez le support avec le hash de la transaction.
