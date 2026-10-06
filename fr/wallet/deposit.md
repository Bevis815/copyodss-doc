# Dépôt

Déposez des USDC / USDT sur votre **compte de trading** CopyOdds pour les utiliser comme capital de copie. Accès : **Wallets → Deposit** → `/wallets/deposit`.

![Page de dépôt](../.gitbook/assets/usdc1_doc.png)

***

## Déposer en quatre étapes

1. **Choisir le réseau** — Polygon (PoS) ou BSC, correspondant au réseau depuis lequel vous retirez sur votre plateforme d'échange  
2. **Choisir l'actif** — **USDC** ou **USDT** uniquement  
3. **Envoyer** — Copiez ou scannez **l'adresse affichée sur cette page**  
4. **Attendre** — Votre solde est mis à jour après la confirmation on-chain ; BSC peut prendre quelques minutes de plus

La page comporte aussi une section **Deposit steps** (étapes de dépôt) reprenant ces quatre étapes, ainsi qu'un lien vers la vidéo **Watch tutorial** (voir le tutoriel) (`/guide-video`). Nous vous recommandons de la regarder avant votre premier dépôt.

### Trois astuces pratiques

| Action | Description |
|--------|-------------|
| **Enregistrer le QR code** | Appuyez sur **Save image** (enregistrer l'image) pour stocker le QR code de l'adresse sur votre téléphone ; scanner est moins sujet aux erreurs que saisir |
| **Copier après avoir choisi le réseau** | Après être passé sur BSC, vous **devez copier à nouveau l'adresse** — les deux chaînes utilisent des adresses différentes |
| **N'utiliser que l'adresse actuellement affichée sur cette page** | N'utilisez pas d'anciennes adresses issues de l'historique de discussion ou envoyées par d'autres personnes |

***

## Règles importantes

| Règle | Description |
|------|-------------|
| Réseaux pris en charge | **Polygon (PoS)** (recommandé) et **BSC** ; la page affiche des étiquettes telles que « Recommandé / Rapide / Frais réduits » |
| L'adresse dépend du réseau | L'adresse en garde Polygon et l'adresse de passerelle BSC sont **différentes** — ne les confondez jamais |
| USDC / USDT uniquement | Les autres jetons ne peuvent généralement pas être crédités |
| N'utilisez pas la mauvaise chaîne | N'utilisez pas de réseaux non pris en charge comme Ethereum / Arbitrum |
| Vérifiez l'adresse | Appuyez sur **Verify deposit address** (vérifier l'adresse de dépôt), et le système vous enverra l'adresse via le **bot Telegram officiel** ou votre **e-mail associé** pour vérification |
| Privilégiez l'USDC | L'USDT sur Polygon est souvent affiché comme « USDT (PoS) » ; ne déposez pas de BNB ni d'autres jetons |

### Comment utiliser Verify deposit address

1. Appuyez sur **Verify deposit address**
2. La page vous invitera à démarrer le bot Telegram officiel (`@botname`) ou à consulter votre e-mail associé
3. Lorsque vous recevez l'adresse, **comparez-la caractère par caractère** avec celle de la page
4. Ne continuez que si elle correspond exactement

### Votre solde comporte deux montants

| Terme | Signification |
|------|---------|
| **Solde on-chain** | Les USDC natifs effectivement arrivés sur la blockchain |
| **Solde négociable** | La partie que la plateforme a traitée et qui peut être utilisée pour la copie |

Si, juste après un dépôt, vous voyez « xx USDC natifs on-chain, conversion automatique en solde négociable », c'est le processus normal — attendez quelques minutes et actualisez.

***

## Détails

1. Connectez-vous et vérifiez que votre compte de trading est actif
2. Sur la page de dépôt, choisissez d'abord le réseau, puis copiez l'adresse
3. Lors du retrait depuis votre plateforme d'échange ou votre portefeuille : vérifiez soigneusement le réseau, le jeton et le montant
4. Revenez sur CopyOdds et tirez pour actualiser votre solde si nécessaire
5. Avant votre premier dépôt important : déposez un petit montant → vérifiez qu'il arrive → puis déposez davantage

***

## Dépôt lent ou manquant ?

Vérifiez dans cet ordre :

1. Le réseau de retrait correspond-il à celui sélectionné sur cette page (Polygon vs BSC) ?
2. Le jeton est-il de l'USDC / USDT ?
3. L'adresse de réception est-elle **exactement identique** à celle de cette page ?
4. La transaction on-chain est-elle confirmée ? (Recherchez le hash sur l'explorateur de blocs correspondant)
5. L'avez-vous envoyé par erreur vers une destination de retrait ou l'adresse d'une autre plateforme ?

Toujours manquant : contactez le support avec le **hash de la transaction, le réseau, le montant, l'heure et votre e-mail d'inscription**.

***

## Que faire après le dépôt ?

- Pour commencer à copier : assurez-vous d'abord que **Polymarket est prêt**, puis **achetez du Gas de la plateforme** (voir [Gas de la plateforme](gas.md))
- Les achats copiés nécessitent des USDC disponibles (au moins environ $1 recommandé)

***

## Où vérifier après l'arrivée des fonds

Ouvrez **Transaction history** (historique des transactions) → `/wallets/ledger` pour voir le réseau, l'actif, le statut et le solde après la transaction du dépôt. Voir [Historique des transactions](ledger.md).
