# Supprimer un membre du restaurant

------

**Nom du cas :** Supprimer un membre du restaurant
**But :** Le patron supprime un membre du restaurant existant  
**Acteur principal :** Patron  
**Date de création :** 26/11/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 26/11/2018  
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Déclenchement :**
Le patron indique qu'il veut supprimer un membre du restaurant.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut supprimer un membre du restaurant.
3. Le système affiche les membres du restaurant existants.
4. Le patron choisit le membre du restaurant à supprimer.
5. Le système demande la confirmation du choix.
6. Le patron confirme le choix du membre du restaurant à supprimer.
7. Le système valide le membre du restaurant à supprimer.
8. Le système supprime le membre du restaurant.
9. Le système indique au patron que le membre du restaurant est supprimé.
10. Fin du scénario.

**Post-conditions :**
- Le membre du restaurant est retiré du système

**Scénarios alternatifs :**
- 6.a. [Le patron infirme la suppression du membre du restaurant choisi]
	- 6.a.1. Le système affiche un message d'erreur.
	- 6.a.2. Retour à l'étape 3.
- 7.a. [Le membre du restaurant choisi n'est pas valide/est déjà supprimé]
	- 7.a.1. Le système affiche un message d'erreur.
	- 7.a.2. Retour à l'étape 3.

**Scénarios d'exception :**
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
