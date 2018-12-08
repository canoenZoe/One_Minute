
# Ajouter un membre du restaurant

------

**Nom du cas :** Ajouter un membre du restaurant  
**But :** Le patron ajoute un nouveau membre du restaurant à son équipe pour que le nouveau membre du restaurant correspondant puisse utiliser l'application.  
**Acteur principal :** Patron  
**Date de création :** 30/11/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 30/11/2018  
**Nom du responsable de la dernière modification :** Sami BARCHID  
**Version :** 1.0

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**


**Déclenchement :**
Le patron indique qu'il veut ajouter un nouveau membre dans le restaurant.

**Scénario nominal :**
1. Début du scénario
2. Le patron indique qu'il veut ajouter un nouveau membre du restaurant.
3. Le système demande au patron d'entrer les données du nouveau membre du restaurant.
4. Le patron entre les données du nouveau membre du restaurant.
5. Le système valide les données du nouveau membre du restaurant.
6. Le système enregistre le nouveau membre du restaurant.
7. Le système indique au patron que le nouveau membre du restaurant a été créé avec succès.
8. Fin du scénario.

**Post-conditions :**
- Le nouveau membre du restaurant est enregistré dans le système.

**Scénarios alternatifs :**
- 5.a. [Les données ne sont pas valides]
	- 5.a.1. Le système affiche un message d'erreur.
	- 5.a.2. Retour à l'étape 3.

**Scénarios d'exception :**
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du scénario.
