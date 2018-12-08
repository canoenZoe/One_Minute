
# Modifier un membre du restaurant

------

**Nom du cas :** Modifier un membre du restaurant  
**But :** La patron modifie un membre du restaurant existant  
**Acteur principal :** Patron  
**Date de création :** 26/11/2018
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 26/11/2018
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1.0

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Déclenchement :**
Le patron indique qu'il veut modifier un membre du restaurant.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut modifier un membre du restaurant.
3. Le système affiche les membres du restaurant existants.
4. Le patron choisit le membre du restaurant à modifier.
5. Le système valide le membre du restaurant à modifier.
6. Le système demande au patron d'entrer les modifications du membre du restaurant.
7. Le patron entre les données de modification du membre du restaurant.
8. Le système valide le membre du restaurant modifié.
9. Le système modifie le membre du restaurant.
10. Le système indique au patron que le membre du restaurant est modifié.
11. Fin du scénario.

**Post-conditions :**
- Le système a enregistré les modifications sur le membre du restaurant.
- Le patron est redirigé vers la liste des membres du restaurant.

**Scénarios alternatifs :**
- 5.a. [Le membre du restaurant choisi n'est pas valide/n'existe pas]
	- 5.a.1. Le système affiche un message d'erreur.
	- 5.a.2. Retour à l'étape 3.
- 8.a. [Données invalides]
	- 8.a.1. Le système affiche un message d'erreur.
	- 8.a.2. Retour à l'étape 6.

**Scénarios d'exception :**
- 3.a. [Il n'y a aucun membre du restaurant existant]
	- 3.a.1. Le système affiche un message d'erreur.
	- 3.a.2. Le système revient à son état d'avant le déclenchement.
	- 3.a.3. Fin du scénario.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
