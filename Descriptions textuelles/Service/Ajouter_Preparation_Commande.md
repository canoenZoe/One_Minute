# Ajouter préparation dans une commande

---

**Nom du cas :** Ajouter une préparation à la commande
**But :** Ajouter une préparation à une commande existante
**Acteur principal :** Serveur
**Date de création :** 06/11/2018
**Nom du responsable de création :** Zoé Canoen
**Dernière date de mise à jour : **
**Nom du responsable de la dernière modification :**
**Version :** 1.0

---

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Le client a déjà commandé une fois auparavant.  

**Déclenchement :** Le cas commence lorsque le client souhaite ajouter des *préparations* à sa commande.

**Scénario nominal :**  

1. Le client fait appel à un serveur afin de changer sa commande.  
2. Le serveur arrive à la table du client.  
3. Le serveur prend sa tablette.  
4. Le serveur sélectionne la liste des commandes en cours.  
5. Le système affiche la liste des commandes en cours.  
6. Le serveur sélectionne la commande du client.  
7. Le système affiche le résumé de la commande sélectionnée.  
8. Le serveur demande au client ce qu'il souhaite commander.
9. Le serveur ajoute la ou les nouvelles *préparations* à la commande.  
10. Le serveur confirme l'ajout de *préparations*.  
11. Le système notifie l'équipe de cuisine que la commande a été modifiée.  

**Post-condition :**
- L'équipe de cuisine est notifiée de la modification de la commande en question.  

**Scénarios alternatifs :**
- 2a. [Aucun serveur n'est disponible]
  - 2a.1 Le client attend qu'un serveur soit de nouveau disponible.
  - 2a.2 Renvoie à 1.

- 9a. [Une ou plusieurs *préparations* demandées ne sont plus disponibles]
  - 9a.1 Le système affiche que la ou les *préparations* ne sont plus disponibles.
  - 9a.2 Le serveur ne peut pas les sélectionner.
  - 9a.3 Renvoie à 8.  

**Scénario d'exception :**
- 5a. [Le système n'est pas connecté à internet]
  - 5a.1 Le système prévient le serveur qu'il ne parvient pas à se connecter à internet.
  - 5a.2 Le système met fin à la session.  


------

### Glossaire :

-
