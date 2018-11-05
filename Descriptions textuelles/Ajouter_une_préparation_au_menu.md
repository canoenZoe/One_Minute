# Ajouter une préparation au menu

------

**Nom du cas :** Ajouter une préparation au menu.
**But :** Le patron ajoute une préparation à un menu qu'il a choisi.
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
- Le patron a choisi le menu sur lequel il veut ajouter une préparation.

**Déclenchement :**
Le patron indique qu'il veut ajouter une préparation au menu choisi.

**Scénario nominal :**
1. Le patron indique qu'il veut ajouter une préparation au menu choisi.
2. Le système affiche les préparations qui peuvent être ajoutées au menu.
3. Le patron choisit la préparation à ajouter.
4. Le système valide la préparation choisie.
5. Le système enregistre la préparation dans le menu.
6. Le Système confirme l'ajout au patron.
7. Fin du CU

**Post-conditions :**
- La préparation choisie est ajoutée au menu.

**Scénarios alternatifs :**
- 3.a. [La préparation à ajouter n'existe pas / existe déjà dans le menu]
	- 3.a.1. La patron indique qu'il veut
	- 3.a.2. Exécuter le CU : "Ajouter une préparation"
	- 3.a.3. Aller à l'étape 4.

- 4.a. [La préparation choisie n'est pas valide]
	- 4.a.1. Le système affiche un message d'erreur.
	- 4.a.2. Retour à l'étape 2.
	
**Scénarios d'exception :**
- 3.b. [Aucune préparation n'existe]
	- 3.b.1. Le système affiche un message d'erreur.
	- 3.b.2. Le système revient à son état d'avant le déclenchement.
	- 3.b.3. Fin du CU.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.