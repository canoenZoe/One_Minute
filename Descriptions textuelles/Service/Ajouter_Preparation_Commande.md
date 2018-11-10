# Ajouter préparation dans une commande

---

**Nom du cas :** Ajouter une préparation à la commande  
**But :** Ajouter une préparation à une commande existante  
**Acteur principal :** Serveur  
**Date de création :** 06/11/2018  
**Nom du responsable de création :** Zoé Canoen  
**Dernière date de mise à jour :** 10/11/2018  
**Nom du responsable de la dernière modification :** Laurine DRODZINSKI  
**Version :** 2.0

---

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Le client a déjà commandé une fois auparavant.  

**Déclenchement :** Le cas commence lorsque le client souhaite ajouter des *préparations* à sa commande.

**Scénario nominal :**  

1. Début du scénario
2. Le client fait appel à un serveur afin de changer sa commande.  
3. Le serveur arrive à la table du client.  
4. Le serveur prend sa tablette.  
5. Le serveur sélectionne la liste des commandes en cours.  
6. Le système affiche la liste des commandes en cours.  
7. Le serveur sélectionne la commande du client.  
8. Le système affiche le résumé de la commande sélectionnée.  
9. Le serveur demande au client ce qu'il souhaite commander.
10. Le serveur ajoute la ou les nouvelles *préparations* à la commande.  
11. Le serveur confirme l'ajout de *préparations*.  
12. Le système notifie l'équipe de cuisine que la commande a été modifiée.
13. Fin du scénario

**Post-condition :**
- L'équipe de cuisine est notifiée de la modification de la commande en question.  

**Scénarios alternatifs :**
- 3a. [Aucun serveur n'est disponible]
  - 3a.1 Le client attend qu'un serveur soit de nouveau disponible.
  - 3a.2 Renvoie à 2.

- 10a. [Une ou plusieurs *préparations* demandées ne sont plus disponibles]
  - 10a.1 Le système affiche que la ou les *préparations* ne sont plus disponibles.
  - 10a.2 Le serveur ne peut pas les sélectionner.
  - 10a.3 Renvoie à 9.  

**Scénario d'exception :**
- 6a. [Le système n'est pas connecté à internet]
  - 6a.1 Le système prévient le serveur qu'il ne parvient pas à se connecter à internet.
  - 6a.2 Le système met fin à la session.  


------

### Glossaire :

-
