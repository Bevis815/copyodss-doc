# Retrait

Retirez les **USDC** librement disponibles de votre compte de trading vers un portefeuille externe. Accès : **Wallets → Withdraw** → `/wallets/withdraw`.

![Page de retrait](../.gitbook/assets/usdc2_doc.png)

![Vérification renforcée du retrait](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Règles de retrait

| Élément | Description |
|------|-------------|
| Réseau | **Polygon (PoS) uniquement** |
| Actif | **USDC** |
| Adresse de réception | Doit pouvoir recevoir des USDC sur Polygon ; **ne saisissez pas** l'adresse en garde de la page de dépôt, et il ne peut pas s'agir de **votre adresse de dépôt actuelle elle-même** |
| Portefeuille de destination | Doit détenir un peu de **MATIC (POL)** ; vous en aurez besoin pour payer le gas lorsque vous déplacerez ces USDC on-chain par la suite |
| Vérification renforcée | Requise pour chaque retrait (voir ci-dessous) |

***

## Étapes

1. Ouvrez la page de retrait et vérifiez le **Max withdrawable** (montant maximal retirable, qui peut être inférieur à votre solde total)
2. Saisissez une adresse de réception Polygon et un montant
3. Vérifiez bien le réseau, l'adresse et le montant
4. Appuyez sur continuer et effectuez la **vérification renforcée du retrait**
5. Après la soumission, suivez le statut dans vos relevés / enregistrements

***

## Pourquoi le « Max withdrawable » est-il inférieur à mon solde ?

Les fonds suivants ne peuvent généralement pas être retirés immédiatement :

- Les fonds immobilisés dans des positions ouvertes
- Les fonds gelés dans des ordres non exécutés
- Les autres marges / fonds bloqués par le système

Fiez-vous au montant **Max withdrawable** affiché sur la page, et non à votre solde total.

***

## Vérification renforcée du retrait

Chaque retrait doit être confirmé avec un code **Authenticator (TOTP)** à 6 chiffres — **c'est actuellement la seule méthode prise en charge**.

Si vous n'en avez pas configuré, le système vous guidera pour l'activer dans les paramètres ; **vous ne pouvez pas retirer sans lui**.

**Les Passkeys et les codes par e-mail ne peuvent pas être utilisés pour confirmer les retraits** (ils servent uniquement à la connexion et à des scénarios similaires).

Voir [Sécurité des retraits](../security/withdrawal-security.md) et [Authentification à deux facteurs (2FA)](../security/2fa.md).

***

## Retrait temporairement impossible ?

| Message | Signification | Que faire |
|---------|---------|------------|
| **Withdrawal channel busy** | De nombreuses demandes de retrait aujourd'hui | Attendez quelques minutes ou quelques heures comme indiqué ; **vos fonds sont en sécurité et vous n'avez pas besoin de soumettre à nouveau la demande** |
| **New device / new network cooldown** | Vous venez de changer d'appareil ou votre IP a changé | Réessayez une fois le délai de carence écoulé |
| **Unfilled orders exist** | Vous avez encore des ordres ouverts | Annulez-les ou attendez leur exécution |
| **Positions still open** | Votre adresse en garde détient encore des positions sur des marchés | Clôturez-les ou attendez le règlement |
| **Previous withdrawal in progress** | Encore en cours de confirmation on-chain | Attendez qu'il se termine avant d'envoyer le suivant |
| **Address is your deposit address** | Vous ne pouvez pas retirer vers votre adresse de dépôt | Utilisez plutôt votre propre adresse de réception |

Vérifiez les sessions et les paramètres de sécurité dans **Settings → Devices / Security**. Si l'échec persiste, contactez le support en précisant si vous avez récemment changé d'appareil.

***

## Conseils de sécurité

- Avant votre premier retrait important : testez d'abord avec un petit montant
- Les retraits ne peuvent généralement pas être annulés une fois soumis — vérifiez l'adresse caractère par caractère
- CopyOdds ne vous contactera jamais par message privé pour « vous aider à effectuer un retrait » et ne vous demandera jamais vos codes de vérification

***

## Où consulter les enregistrements de retrait

**Transaction history** (historique des transactions) → `/wallets/ledger` affiche le statut de chaque retrait et le « solde après », avec un lien vers l'explorateur de blocs. Voir [Historique des transactions](ledger.md).
