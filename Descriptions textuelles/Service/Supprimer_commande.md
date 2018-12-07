# Suivre une commande

------

**Nom du cas :** Supprimer une commande
**But :** Le serveur souhaite supprimer une commande
**Acteur principal :** Serveur  
**Date de création :** 07/12/2018
**Nom du responsable de création :** Zoé Canoen
**Dernière date de mise à jour :** 
**Nom du responsable de la dernière modification :** 
**Version :** 1.0

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- La commande doit exister

**Déclenchement :** 

- Le serveur souhaite supprimer une commande, par exemple si un client s'en va sans payer.

**Scénario nominal :** 

1. Début du scénario
2. Le serveur indique qu'il souhaite supprimer la commande
3. Le système lui demande de valider son choix 
4. Le serveur valide
5. Le système supprime les plats qui étaient en préparations avec la commande
6. Le système notifie la cuisine qu'une commande a été annulée 
7. Le système supprime la commande dans la liste des commandes
8. Fin du scénario

**Post-condition :**

- Aucune

**Scénario alternatif :**  

- Aucun

**Scénario d'exception :**  

- Aucun
