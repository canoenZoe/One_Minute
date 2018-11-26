
# Créer une catégorie

------

**Nom du cas :** Créer une catégorie
**But :** Le patron crée une nouvelle catégorie
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

**Déclenchement :**
Le patron indique qu'il veut créer une catégorie.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut créer une catégorie.
3. Le système demande au patron d'entrer les données de la catégorie.
4. Le patron entre les données de la catégorie.
5. Le système valide les données de la catégorie.
6. Le système enregistre la nouvelle catégorie.
7. Le système indique au patron que la catégorie a été créée avec succès.
8. Fin du scénario.

**Post-conditions :**
- La nouvelle catégorie est enregistrée dans le système.
- La nouvelle catégorie peut être référencée dans les préparations.

**Scénarios alternatifs :**
- 5.a. [Les données ne sont pas valides]
	- 5.a.1. Le système affiche un message d'erreur.
	- 5.a.2. Retour à l'étape 3.

**Scénarios d'exception :**
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
