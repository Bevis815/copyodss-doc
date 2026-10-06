# Appareils et Passkeys

Cette page aborde deux sujets de sécurité : **quels appareils se sont connectés à votre compte**, et **comment vous connecter rapidement avec Face ID / l'empreinte digitale**.

Accès : Settings → Security → **Devices** → `/settings/devices` ; les Passkeys se gèrent dans Settings → `/settings/passkeys`

***

## 1. Appareils

### Ce que vous verrez

| Champ | Signification |
|-------|---------|
| Nom de l'appareil | par ex. le modèle de votre téléphone ou le nom du système d'exploitation ; affiche « Unknown device » s'il ne peut pas être identifié |
| **Current device** | Celui que vous utilisez en ce moment |
| **Last active** | Sa dernière utilisation |
| Sessions actives | Le nombre de sessions de connexion sur cet appareil |
| Retrait disponible à partir de | Les nouveaux appareils doivent généralement attendre un certain temps avant de pouvoir retirer |

### Supprimer un appareil

1. Trouvez un appareil que vous ne reconnaissez pas → appuyez sur **Remove** (supprimer)
2. Après confirmation, l'appareil est supprimé et **ses sessions de connexion sont immédiatement invalidées**

### Quand en supprimer un

- Vous avez changé de téléphone / d'ordinateur et l'ancien appareil est toujours listé
- Il y a dans votre historique de connexion un appareil que vous ne reconnaissez pas
- Vous soupçonnez quelqu'un d'autre d'utiliser votre compte

> Après la suppression, cet appareil doit se reconnecter (code par e-mail / Telegram / Passkey).

***

## 2. Passkeys

Une Passkey vous permet de vous connecter avec **Face ID, l'empreinte digitale ou le verrouillage d'écran** de votre téléphone au lieu de saisir un code.

### Ajouter une Passkey

1. Settings → Passkeys → **Add passkey** (ajouter une passkey)
2. Effectuez la vérification Face ID / empreinte digitale comme indiqué
3. Une fois terminé, la Passkey apparaît dans la liste avec sa date de création, sa dernière utilisation et son état de synchronisation

### L'utiliser pour se connecter

Choisissez **Passkey** sur la page de connexion — aucun e-mail nécessaire.

### Supprimer une Passkey

Sélectionnez-la → **Delete** (supprimer) → confirmez. Après la suppression, cet appareil ne peut plus se connecter avec une Passkey.

### Dépannage

| Symptôme | Que faire |
|---------|------------|
| Face ID ne s'affiche pas lors de l'ajout | Annulez et **appuyez à nouveau sur « Add Passkey »**, en effectuant la vérification dès que l'invite apparaît ; fermez d'abord les bannières de notification |
| Message indiquant que cet appareil n'est pas pris en charge | Utilisez le navigateur intégré du système (Safari sur iOS, Chrome sur Android), ou utilisez simplement un code par e-mail |
| Message indiquant qu'une Passkey du même nom existe déjà | Supprimez d'abord l'ancienne entrée « Android device » ; si vous utilisez un proxy / VPN, désactivez-le et réessayez |
| La connexion échoue | Connectez-vous plutôt avec un code par e-mail ; un échec de Passkey n'affecte pas la sécurité de votre compte |

> Les Passkeys ne peuvent être utilisées que pour la connexion et **ne peuvent pas servir à la vérification des retraits**.
