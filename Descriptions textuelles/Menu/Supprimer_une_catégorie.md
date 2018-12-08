# Supprimer une catégorie

------

**Nom du cas :** Supprimer une catégorie  
**But :** Le patron supprime une catégorie existante  
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
Le patron indique qu'il veut supprimer une catégorie.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut supprimer une catégorie.
3. Le système affiche les catégories existantes.
4. Le patron choisit la catégorie à supprimer.
5. Le système demande la confirmation du choix.
6. Le patron confirme le choix de la catégorie à supprimer.
7. Le système valide la catégorie à supprimer.
8. Le système supprime la catégorie.
9. Le système indique au patron que la catégorie est supprimée.
10. Fin du scénario.

**Post-conditions :**
- La catégorie est retirée du système

**Scénarios alternatifs :**
- 6.a. [Le patron infirme la suppression de la catégorie choisie]
	- 6.a.1. Le système affiche un message d'erreur.
	- 6.a.2. Retour à l'étape 3.
- 7.a. [La catégorie choisie n'est pas valide/est déjà supprimée]
	- 7.a.1. Le système affiche un message d'erreur.
	- 7.a.2. Retour à l'étape 3.
- 7.b. [La catégorie choisie est référencée dans au moins une préparation]
	- 7.b.1. Le système indique au patron que la catégorie est utilisée dans une/des préparation(s).
	- 7.b.2. Le système affiche les préparations où la catégorie est utilisée.
	- 7.b.3. Le patron confirme la suppression de la catégorie.
	- 7.b.4. Le système supprime les références des préparations vers la catégorie à supprimer.
	- 7.b.5. Aller à l'étape 8.

**Scénarios d'exception :**
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
