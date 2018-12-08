# Consulter un menu

------

**Nom du cas :** Consulter un menu  
**But :** Le patron consulte un menu pour l'administrer  
**Acteur principal :** Patron  
**Date de création :** 19/10/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 26/11/2018  
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1.0

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Le patron consulte la liste des menus créés.

**Déclenchement :**
Le patron sélectionne le menu qu'il veut afficher pour l'administrer.

**Scénario nominal :**
1. Début du scénario
2. Le patron sélectionne le menu qu'il veut afficher pour l'administrer.
3. Le système valide le menu sélectionné.
4. Le système affiche le menu sélectionné.
5. Fin du scénario.

**Post-conditions :**


**Scénarios alternatifs :**
- 3.a. [Le menu est introuvable]
	- 3.a.1. Le système affiche un message d'erreur.
	- 3.a.2. retour à l'étape 1.

**Scénarios d'exception :**
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
