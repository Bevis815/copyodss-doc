# Paramètres

Accès : **Settings** (paramètres) → `/settings`

La page Paramètres regroupe en un seul endroit tous les réglages autres que ceux du copy trading. Si vous n'êtes pas connecté, vous ne verrez qu'une invitation à vous connecter.

***

## 1. Général

| Élément | Description |
|------|-------------|
| **Language** | Changer la langue de l'interface ; l'URL reçoit ensuite un préfixe de langue (par ex. `/zh`) |
| **Name** | Saisissez votre prénom et votre nom pour aider le support à vérifier votre identité |

***

## 2. Copy trading

- **Adresse de trading en garde** : ouverte automatiquement après la connexion ; c'est votre adresse réelle de réception / de trading
- Si elle indique « pas encore ouverte », suivez les instructions pour l'ouvrir sur cette page avant de déposer
- Lors de la première utilisation : parcourez le processus avec un petit dépôt + un petit retrait avant d'utiliser des montants plus importants

***

## 3. Notifications

Vous pouvez activer ou désactiver chaque type d'alerte séparément :

| Catégorie | Alertes |
|----------|--------|
| Trading | Ordre du trader détecté, ordre soumis, ordre échoué, ordre exécuté, ordre annulé |
| Budget et limites | Avertissement de budget, solde insuffisant |
| Système | Récupération automatique, session sur le point d'expirer |

> Les préférences prennent effet dès leur enregistrement ; des canaux plus avancés comme les notifications push en temps réel sont déployés progressivement, et la page indiquera leur statut actuel.

***

## 4. Liaison de comptes

| Liaison | Objectif |
|------|---------|
| **Email** | Recevoir des codes pour se connecter ; une fois lié, vous pouvez vous connecter par e-mail ou par Telegram |
| **Telegram** | Se connecter avec Telegram |
| **Web3 wallet** | Enregistrer les informations de votre portefeuille externe |

> Si l'e-mail / le compte Telegram que vous liez appartient déjà à un autre compte, la liaison **conserve le compte actuel**, et l'autre compte ne peut plus se connecter de cette manière.

***

## 5. Sécurité

Une carte de statut de sécurité du compte :

| Élément | Description |
|------|-------------|
| **Active sessions** | Nombre de sessions de connexion en cours et leur expiration |
| **Devices** | Gérer les appareils sur lesquels vous vous êtes connecté ; voir [Appareils et Passkeys](devices-and-passkeys.md) |
| **Terms status** | Si vous avez accepté le contrat d'utilisation |
| **Trading status** | Normal / Restreint |
| **Withdrawal verification** | Description de la méthode de vérification renforcée requise avant un retrait |

### Vérification renforcée des retraits

Vous devez confirmer votre identité avant chaque retrait. **Actuellement, seuls les codes Authenticator sont pris en charge** ; s'il n'est pas associé, activez-le d'abord dans les paramètres. Les Passkeys et les codes par e-mail ne peuvent pas être utilisés pour les retraits.

***

## 6. À propos

| Accès | Contenu |
|-------|---------|
| **User Agreement** | `/settings/terms` |
| **Privacy Policy** | `/settings/privacy` |
| **Version** | `/settings/version` — voir la version actuelle, si une nouvelle version est disponible, et le téléchargement Android |

***

## 7. Déconnexion

Vous pouvez vous déconnecter en bas de la page Paramètres. Après la déconnexion, vous devrez vous reconnecter pour utiliser le copy trading, le portefeuille et les autres fonctionnalités ; vos règles elles-mêmes ne sont pas supprimées.
