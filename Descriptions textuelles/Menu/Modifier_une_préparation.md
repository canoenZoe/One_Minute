# Modifier une préparation

------

**Nom du cas :** Modifier une préparation.
**But :** La patron modifie une préparation existante.
**Acteur principal :** Patron
**Date de création :** 19/10/2018
**Nom du responsable de création :** Sami BARCHID
**Dernière date de mise à jour : **05/11/2018
**Nom du responsable de la dernière modification :** Sami BARCHID
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Le patron est authentifié dans le système.

**Déclenchement :**
Le patron indique qu'il veut modifier une préparation.

**Scénario nominal :**
1. Le patron indique qu'il veut modifier une préparation.
2. Le système affiche les préparations existantes.
3. Le patron choisit la préparation à modifier.
4. Le système valide la préparation à modifier.
5. Le système demande au patron d'entrer les modifications.
6. Le patron entre les données de modification de la préparation.
7. Le système valide la préparation modifiée.
8. Le système modifie la préparation.
9. Le système indique au patron que la préparation est modifiée.
10. Fin du CU.

**Post-conditions :**
- La préparation est modifiée.

**Scénarios alternatifs :**
- 4.a. [La préparation choisie n'est pas valide/n'existe pas]
	- 4.a.1. Le système affiche un message d'erreur.
	- 4.a.2. Retour à l'étape 2.
- 7.a. [Données invalides]
	- 7.a.1. Le système affiche un message d'erreur.
	- 7.a.2. Retour à l'étape 5.
	
**Scénarios d'exception :**
- 2.a. [Il n'y a aucune préparation existante]
	- 2.a.1. Le système affiche un message d'erreur.
	- 2.a.2. Le système revient à son état d'avant le déclenchement.
	- 2.a.3. Fin du CU.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.
	
