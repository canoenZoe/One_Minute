# Ajouter une préparation au menu

------

**Nom du cas :** Ajouter une préparation au menu  
**But :** Le patron ajoute une préparation à un menu qu'il a choisi  
**Acteur principal :** Patron  
**Date de création :** 19/10/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 05/11/2018  
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Le patron a choisi le menu sur lequel il veut ajouter une préparation.

**Déclenchement :**
Le patron indique qu'il veut ajouter une préparation au menu choisi.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut ajouter une préparation au menu choisi.
3. Le système affiche les préparations qui peuvent être ajoutées au menu.
4. Le patron choisit la préparation à ajouter.
5. Le système valide la préparation choisie.
6. Le système enregistre la préparation dans le menu.
7. Le système confirme l'ajout au patron.
8. Fin du scénario

**Post-conditions :**
- La préparation choisie est ajoutée au menu.

**Scénarios alternatifs :**
- 4.a. [La préparation à ajouter n'existe pas / existe déjà dans le menu]
	- 4.a.1. La patron indique qu'il veut
	- 4.a.2. Exécuter le CU : "Ajouter une préparation"
	- 4.a.3. Aller à l'étape 5.

- 5.a. [La préparation choisie n'est pas valide]
	- 5.a.1. Le système affiche un message d'erreur.
	- 5.a.2. Retour à l'étape 3.

**Scénarios d'exception :**
- 4.b. [Aucune préparation n'existe]
	- 4.b.1. Le système affiche un message d'erreur.
	- 4.b.2. Le système revient à son état d'avant le déclenchement.
	- 4.b.3. Fin du scénario.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
