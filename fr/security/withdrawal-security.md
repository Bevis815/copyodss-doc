# Sécurité des retraits

Les retraits transfèrent des fonds vers une adresse externe, c'est pourquoi chaque retrait nécessite une **vérification renforcée**. Actuellement, seul l'**Authenticator (TOTP)** est pris en charge.

![Vérification renforcée du retrait](../.gitbook/assets/withdraw_stepup_doc.png)

***

## Méthode de vérification

- **La seule méthode : un code Authenticator** (Google / Microsoft Authenticator, 1Password, etc.)
- Si aucun Authenticator n'est associé, le processus de retrait vous demandera d'en activer un d'abord dans les paramètres
- **Les Passkeys et les codes par e-mail ne peuvent pas être utilisés pour les retraits** (ils fonctionnent toujours pour la connexion, etc.)

Vous trouverez la description de la « vérification renforcée des retraits » dans les paramètres.

***

## Que faire lors d'un retrait

1. Assurez-vous qu'un Authenticator est associé
2. Renseignez l'adresse Polygon et le montant sur la page de retrait, et vérifiez-les bien
3. Dans la fenêtre de vérification renforcée, saisissez le code à 6 chiffres
4. Soumettez le retrait une fois la vérification réussie

Si le code est erroné ou expiré, saisissez simplement à nouveau le code actuel.

***

## Protections supplémentaires

| Mécanisme | Description |
|-----------|-------------|
| Max withdrawable | Les fonds immobilisés dans des positions et des ordres ne peuvent pas être retirés |
| Délai de carence nouvel appareil / nouveau réseau | Les retraits peuvent être temporairement indisponibles après un changement d'appareil ou d'IP |
| Canal de retrait saturé | Aux heures de pointe, vous devrez peut-être attendre de quelques minutes à quelques heures ; vos fonds sont en sécurité |
| Le portefeuille de destination a besoin de MATIC | Conservez un peu de MATIC (POL) sur la nouvelle adresse, sinon vous ne pourrez pas déplacer ces USDC on-chain par la suite |
| Restrictions de trading | Si le trading du compte est restreint, les retraits peuvent également être affectés |
| Vérification de l'adresse | Les fonds envoyés à une mauvaise adresse externe ne peuvent généralement pas être récupérés |

***

## Conseils de sécurité

- Ne donnez jamais votre code Authenticator à quelqu'un qui prétend faire partie du support
- Ne remplacez jamais l'adresse de retrait par une « adresse intermédiaire » que quelqu'un vous fournit
- Pour les indications concernant le domaine de messagerie officiel, consultez [Anti-hameçonnage](anti-phishing.md)
- Avant un retrait important : testez avec un petit montant → vérifiez qu'il arrive → puis retirez davantage
