# Mes positions et historique des trades

Une fois que vous avez commencé à copier, toutes vos positions et le résultat de chaque ordre se trouvent sur ces deux pages. **En tant que débutant, ces deux pages sont tout ce que vous devez connaître.**

| Page | Accès | Ce à quoi elle répond |
|------|-------|-----------------|
| **My positions** | My positions → `/executions/positions` | Que détiens-je actuellement, et suis-je en gain ou en perte ? |
| **Trade history** | Executions → `/executions/records` | Le résultat de chaque tentative de copie |
| **Profit/Loss** | Executions → Profit/Loss → `/executions/daily-pnl` | Combien ai-je gagné sur cette période ? |

***

## Mes positions

### Ce que vous verrez

| Champ | Signification |
|-------|---------|
| **Market / Outcome** | Quel événement et quelle issue (Oui / Non) vous avez achetés |
| **Avg. price / Current price** | Votre coût d'entrée et le prix actuel du marché |
| **Cost / Value / P&L** | Combien vous avez dépensé, ce que cela vaut maintenant et si vous êtes en gain |
| **Copy sources** | Quelles règles de copie ont constitué cette position |
| **Status** | Open / Pending settlement / Settled / Archived |

### Ce que vous pouvez faire

| Action | Description |
|--------|-------------|
| **Buy more** | Acheter un peu plus vous-même en saisissant un montant en USD |
| **Close** | Vendre au prix du marché pour verrouiller le P&L ; le prix évolue avec le marché |
| **Bulk close** | Clôturer jusqu'à un certain nombre de positions à la fois |
| **Redeem** | Le marché est terminé et vous avez gagné — convertissez la position en USDC |
| **View details** | Voir l'heure d'achat, le mode de règlement et la chronologie complète |

### Signification des statuts

| Statut | Description |
|--------|-------------|
| **Open** | Le marché n'est pas terminé ; vous pouvez vendre |
| **Pending settlement** | Impossible de vendre pour l'instant ; si vous avez gagné, Redeem apparaîtra ; si vous avez perdu, la position se clôture automatiquement |
| **Settled** | Converti en USDC et reversé sur votre solde |
| **Archived** | Positions minuscules ou illiquides qui ne peuvent pas être vendues pour l'instant ; n'affecte rien d'autre |

***

## Historique des trades (historique des copies)

Chaque ligne correspond à une tentative effectuée par le système en votre nom :

| Statut | Signification |
|--------|---------|
| **Filled** | Copié avec succès |
| **In progress** | Traitement en cours |
| **Skipped** | Aucun ordre passé (voir la raison de l'échec) |
| **Failed** | L'ordre a été rejeté ou a rencontré une erreur |

Vous pouvez filtrer par **Filled / Settled / Unsuccessful**. Appuyez sur n'importe quelle ligne pour voir : la règle de copie, l'ID de l'ordre, le prix d'achat et le nombre de parts, le mode de clôture (vendu / récupéré / expiré), le coût, le produit, le P&L, la chronologie complète et le hash on-chain.

***

## Page Profit/Loss

- Le haut affiche une **courbe du P&L cumulé**, avec possibilité de basculer entre 1 jour / 1 semaine / 1 mois, etc.
- Le bas affiche une **ventilation par période**, incluant aujourd'hui, hier et la variation du P&L du compte pour chaque jour
- La courbe suit la méthodologie de P&L de compte de Polymarket ; si les données officielles sont temporairement indisponibles, la page indiquera qu'elle utilise à la place les données du registre de la plateforme

> L'heure de début du jour ouvré est celle indiquée sur la page (par ex. à partir de 08:00) ; gardez-le à l'esprit lorsque vous consultez des données sur plusieurs jours.

***

## Questions fréquentes des débutants

**Pourquoi le P&L de mes positions ne correspond-il pas à mon solde ?**  
Le P&L des positions est « estimé au prix actuel du marché », et la partie latente varie avec le prix ; votre solde n'en tient compte qu'une fois que vous vendez ou récupérez.

**Pourquoi ma vente a-t-elle échoué ?**  
Raisons courantes : aucun ordre d'achat sur le marché à ce moment-là, parts immobilisées dans des ordres ouverts, ou position restante inférieure à la taille minimale de vente. Réessayez plus tard.

**J'ai gagné — pourquoi ne vois-je pas l'argent ?**  
Le crédit prend un peu de temps après le règlement du marché ; vous pouvez appuyer sur **Redeem** (récupérer) pour récupérer manuellement. Tant que « Pending settlement » est affiché, vous ne pouvez pas encore agir.
