# Retirer une préparation au menu

------

**Nom du cas :** Retirer une préparation au menu  
**But :** Le patron retire une préparation à un menu qu'il a choisi  
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

- Le patron consulte en détails le menu sur lequel il veut retirer une préparation.

**Déclenchement :**

Le patron indique qu'il veut retirer une préparation au menu.

**Scénario nominal :**

1. Le patron indique qu'il veut retirer une préparation au menu.
2. Le système affiche les préparations du menu.
3. Le patron choisit la préparation à retirer.
4. Le système demande la confirmation au patron.
5. Le patron confirme le choix de la préparation à retirer.
6. Le système valide la préparation choisie.
7. Le système supprime la préparation du menu.
8. Le système enregistre la suppression par le patron.
9. Fin du CU.

**Post-condition :**

- La préparation choisie est retirée du menu.

**Scénarios alternatifs :**

- 5.a. [Le patron infirme la préparation à retirer]
	- 5.a.1. Le système affiche un message d'erreur.
	- 5.a.2. Le système revient à son état d'avant le déclenchement.
	- 5.a.3. Retour à l'étape 2.

- 6.a. [La préparation choisie n'est pas valide / est déjà retirée]
	- 6.a.1. Le système affiche un message d'erreur.
	- 6.a.2. Le système revient à son état d'avant le déclenchement.
	- 6.a.3. Retour à l'étape 2.

**Scénarios d'exception :**

- 2.b. [Aucune préparation n'existe dans le menu]
	- 2.b.1. Le système affiche un message d'erreur.
	- 2.b.2. Le système revient à son état d'avant le déclenchement.
	- 2.b.3. Fin du CU.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.
