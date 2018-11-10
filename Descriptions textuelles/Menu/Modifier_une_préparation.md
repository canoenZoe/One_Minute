# Modifier une préparation

------

**Nom du cas :** Modifier une préparation  
**But :** La patron modifie une préparation existante  
**Acteur principal :** Patron  
**Date de création :** 19/10/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 05/11/2018  
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1.0

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Déclenchement :**
Le patron indique qu'il veut modifier une préparation.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut modifier une préparation.
3. Le système affiche les préparations existantes.
4. Le patron choisit la préparation à modifier.
5. Le système valide la préparation à modifier.
6. Le système demande au patron d'entrer les modifications.
7. Le patron entre les données de modification de la préparation.
8. Le système valide la préparation modifiée.
9. Le système modifie la préparation.
10. Le système indique au patron que la préparation est modifiée.
11. Fin du scénario.

**Post-conditions :**
- La préparation est modifiée.

**Scénarios alternatifs :**
- 5.a. [La préparation choisie n'est pas valide/n'existe pas]
	- 5.a.1. Le système affiche un message d'erreur.
	- 5.a.2. Retour à l'étape 3.
- 8.a. [Données invalides]
	- 8.a.1. Le système affiche un message d'erreur.
	- 8.a.2. Retour à l'étape 6.

**Scénarios d'exception :**
- 3.a. [Il n'y a aucune préparation existante]
	- 3.a.1. Le système affiche un message d'erreur.
	- 3.a.2. Le système revient à son état d'avant le déclenchement.
	- 3.a.3. Fin du scénario.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
