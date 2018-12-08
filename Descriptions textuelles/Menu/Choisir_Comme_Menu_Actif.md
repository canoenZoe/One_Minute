
# Choisir comme menu actif

------

**Nom du cas :** Choisir comme menu actif  
**But :** Le patron choisit un menu qui sera actif, et donc sera le menu utilisé dans le restaurant.  
**Acteur principal :** Patron  
**Date de création :** 26/11/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 26/11/2018  
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1.0

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Il y a au moins un menu disponible
- Le patron consulte la liste des menus existants

**Déclenchement :**
Le patron sélectionne le menu qu'il veut choisir comme actif

**Scénario nominal :**
1. Début du scénario
2. Le patron sélectionne le menu qu'il veut choisir comme actif
3. Le système demande la confirmation.
4. Le patron confirme la sélection du menu.
5. Le système valide le menu sélectionné.
6. Le système enregistre le menu sélectionné comme actif.
7. Le système affiche un message de succès.
8. Fin du scénario.

**Post-conditions :**
- Le menu est enregistré comme actif dans le système.

**Scénarios alternatifs :**
- 4.a. [Le patron refuse la confirmation]
	- 4.a.1. Le système retourne à son état d'avant le déclenchement.
	- 4.a.2. Retour en 1.
- 5.a. [Sélection impossible (menu introuvable, invalide, ...)]
	- 5.a.1. Le système affiche un message d'erreur adéquat.
	- 5.a.2. Le système retourne à son état d'avant le déclenchement.
	- 5.a.3. Retour en 1.

- 2.a. [Il existe déjà un menu actif dans le système]
	- 2.a.1. Le système rappelle qu'il existe déjà un menu actif.
	- 2.a.2. Continuer à l'étape 3.

**Scénarios d'exception :**
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
