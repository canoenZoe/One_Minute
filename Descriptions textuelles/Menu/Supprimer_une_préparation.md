# Supprimer une préparation

------

**Nom du cas :** Supprimer une préparation.
**But :** Le patron supprime une préparation existante.
**Acteur principal :** Patron
**Date de création :** 19/10/2018
**Nom du responsable de création :** Sami BARCHID
**Dernière date de mise à jour : **05/11/2018
**Nom du responsable de la dernière modification :** Sami BARCHID
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Déclenchement :**
Le patron indique qu'il veut supprimer une préparation.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut supprimer une préparation.
3. Le système affiche les préparations existantes.
4. Le patron choisit la préparation à supprimer.
5. Le système demande la confirmation du choix.
6. Le patron confirme le choix de la préparation à supprimer.
7. Le système valide la préparation à supprimer.
8. Le système supprime la préparation.
9. Le système indique au patron que la préparation est supprimée.
10. Fin du CU.

**Post-conditions :**
- La préparation est retirée du système

**Scénarios alternatifs :**
- 6.a. [Le patron infirme la suppression de la préparation choisie]
	- 6.a.1. Le système affiche un message d'erreur.
	- 6.a.2. Retour à l'étape 2.
- 7.a. [La préparation choisie n'est pas valide/est déjà supprimée]
	- 7.a.1. Le système affiche un message d'erreur.
	- 7.a.2. Retour à l'étape 2.
- 7.b. [La préparation choisie est utilisée dans un/des menu(s)]
	- 7.b.1. Le système indique au patron que la préparation est utilisée dans un/des menu(s).
	- 7.b.2. Le système affiche les menus où la préparation est utilisée.
	- 7.b.3. Le patron confirme la suppression de la préparation.
	- 7.b.4. Aller à l'étape 7.

**Scénarios d'exception :**
- 7.b.3.a. [Le patron refuse la suppression de la préparation]
	- 7.b.3.a.1. Le système annule la suppression de la préparation.
	- 7.b.3.a.2. Le système retourne à son état d'avant le déclenchement.
	- 7.b.3.a.3. Fin du CU.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.
