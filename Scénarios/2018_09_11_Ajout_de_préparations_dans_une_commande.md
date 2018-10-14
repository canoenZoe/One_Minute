***Nom du cas :*** Ajout de *préparations* dans une commande  
***But :*** Ce cas montre les étapes permettant au serveur d'ajouter des *préparations* dans une commande déjà en cours lorsque le client le désire.  
***Acteur principal :*** Le serveur    
***Date de création :*** 11/09/2018  
***Date de mise à jour :*** 14/10/2018  
***Nom du responsable :*** Laurine Drodzinski   
***Version :*** 2.0

---

***Pré-conditions :***  
Le client a déjà commandé une fois auparavant.  
Le serveur est authentifié dans le système.  
  
***Déclenchement :*** Le cas commence lorsque le client souhaite ajouter des *préparations* à sa commande.   
  
***Scénario nominal :***  
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
  
***Post-condition :*** L'équipe de cuisine est notifiée de la modification de la commande en question.  
  
***Scénarios alternatifs :***  
- 2a. [Aucun serveur n'est disponible]
  - 2a.1 Le client attend qu'un serveur soit de nouveau disponible.
  - 2a.2 Renvoie à 1.
  
- 9a. [Une ou plusieurs *préparations* demandées ne sont plus disponibles]
  - 9a.1 Le système affiche que la ou les *préparations* ne sont plus disponibles.
  - 9a.2 Le serveur ne peut pas les sélectionner.
  - 9a.3 Renvoie à 8.  
   
***Scénario d'exception :***  
- 5a. [Le système n'est pas connecté à internet]
  - 5a.1 Le système prévient le serveur qu'il ne parvient pas à se connecter à internet.
  - 5a.2 Le système met fin à la session.  
    
---

### Glossaire :

- *préparation* : Entrée / Plat / Dessert / Boisson
