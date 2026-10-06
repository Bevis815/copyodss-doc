# Sécurité du portefeuille

CopyOdds utilise un modèle de **compte de trading en garde** : vous n'avez pas besoin de protéger vous-même les clés privées de trading, mais vous devez protéger vos méthodes de connexion et la vérification de vos retraits.

Description complète dans l'App : **Asset security guarantee** (garantie de sécurité des actifs) → `/wallets/security`.

![Garantie de sécurité des actifs](../.gitbook/assets/wallet_security_doc.png)

***

## Mécanismes clés

| Capacité | Description |
|------------|-------------|
| **Portefeuille dédié** | Chaque utilisateur dispose d'un portefeuille en garde distinct ; les actifs sont gérés de manière isolée |
| **Isolation des clés privées** | Les clés privées des portefeuilles sont chiffrées et isolées séparément, et ne sont jamais exposées directement à l'interface de trading courante |
| **Protection des retraits** | Les retraits nécessitent une vérification renforcée ; la modification des paramètres de sécurité clés peut déclencher une nouvelle vérification / un délai de carence |

***

## Garantie de sécurité de la plateforme (résumé)

Si des actifs d'utilisateurs sont perdus en conséquence directe d'un incident de sécurité de la **plateforme CopyOdds elle-même**, comme une vulnérabilité de sécurité ou une intrusion sur un serveur, la plateforme fournira une indemnisation conformément à sa politique de garantie de sécurité (sous réserve de la page produit et des conditions légales).

Veuillez noter :

- La plateforme ne vous demandera **jamais** votre phrase de récupération, votre clé privée, votre mot de passe ou vos codes de vérification par message privé, e-mail ou via le support
- Les pertes de trading sur les marchés prédictifs, les erreurs des utilisateurs (mauvaise chaîne, mauvaise adresse), les escroqueries par hameçonnage, etc. ne sont pas couvertes par « l'indemnisation en cas d'incident de sécurité de la plateforme »
- Utilisez toujours le domaine officiel

***

## Ce que vous devez faire vous-même

1. N'utilisez que le site web / l'App officiels : **copyodds.io**
2. **Activez l'Authenticator** (obligatoire pour les retraits ; voir [Authentification à deux facteurs (2FA)](2fa.md))
3. Ajoutez éventuellement une Passkey pour vous connecter plus facilement
4. Consultez régulièrement vos [appareils connectés](../account/devices-and-passkeys.md) et supprimez ceux que vous ne reconnaissez pas
5. Déposez en utilisant l'adresse de la page, et vérifiez-la avec **Verify deposit address**
6. Testez votre premier dépôt et votre premier retrait avec de petits montants

***

## Pages associées

- Dépôt / Retrait : `/wallets/deposit`, `/wallets/withdraw`
- Paramètres de sécurité : `/settings`
- Gestion des appareils : `/settings/devices`
- Passkeys : `/settings/passkeys`

***

## Vous voulez vérifier par vous-même ?

- Mouvements de fonds et dépenses de Gas : **Transaction history** → `/wallets/ledger` (voir [Historique des transactions](../wallet/ledger.md))
- Appareils sur lesquels vous vous êtes connecté et délais de carence des retraits : **Settings → Devices** → `/settings/devices` (voir [Appareils et Passkeys](../account/devices-and-passkeys.md))
