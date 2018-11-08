# Créer une préparation

------

**Nom du cas :** Créer une préparation  
**But :** Le patron ajoute une préparation  
**Acteur principal :** Patron  
**Date de création :** 19/10/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 05/11/2018  
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Déclenchement :**
Le patron indique qu'il veut créer une préparation.

**Scénario nominal :**
1. Le patron indique qu'il veut créer une préparation.
2. Le système demande au patron d'entrer les données de la préparation.
3. Le patron entre les données de la préparation.
4. Le système valide les données de la préparation.
5. Le système enregistre la nouvelle préparation.
6. Le système indique au patron que la préparation est créée.
7. Fin du CU.

**Post-conditions :**
- La nouvelle préparation est créée dans le système.
- La nouvelle préparation peut être créée dans des menus.

**Scénarios alternatifs :**
- 4.a. [Les données ne sont pas valides / La préparation entrée existe déjà]
	- 4.a.1. Le système affiche un message d'erreur.
	- 4.a.2. Retour à l'étape 2.

**Scénarios d'exception :**
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.
