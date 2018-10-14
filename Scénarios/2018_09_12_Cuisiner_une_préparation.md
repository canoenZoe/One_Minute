***Nom du cas :*** Cuisiner une préparation  
***But :*** Ce cas montre les étapes permettant au cuisinier de s'occuper d'une préparation.
***Acteur principal :*** Le cuisinier    
***Date de création :*** 11/09/2018  
***Date de mise à jour :*** 14/10/2018  
***Nom du responsable :*** Laurine Drodzinski   
***Version :*** 2.0

---

***Pré-conditions :***  
Des commandes sont en cours.
  
***Déclenchement :*** Le cas commence lorsque le cuisinier souhaite souhaite s'occuper d'une ou plusieurs *préparations*.   
  
***Scénario nominal :***  
1. Le cuisinier sélectionne la liste des *préparations* en cours.  
2. Le système affiche la liste des *préparations* en cours.  
3. Le cuisinier choisit une ou plusieurs *préparations* qu'il s'apprête à cuisiner.  
4. Le cuisinier sélectionne son nom dans la liste des cuisiniers.  
5. Le cuisinier valide son choix.  
6. Le système réserve la ou les *préparations* choisies afin qu'aucun autre cuisinier ne puisse les sélectionner.  
7. Le cuisinier commence a cuisiner.  
8. Le cuisinier termine la ou les *préparations*.
9. Le cuisinier indique au système qu'il a terminé les *préparations*.
10. Le cuisinier indique au système qu'une *partie de commande* est terminée. 
  
***Post-condition :*** Les serveurs sont notifiés afin qu'ils puissent servir une *partie de commande*. Le scénario ***Servir une commande*** peut être réalisé. 
  
***Scénarios alternatifs :***  
- 3a. [Le cuisinier se rend compte qu'il n'est plus possible de réaliser une ou plusieurs *préparations*]
  - 3a.1 Le cuisinier indique au système qu'une ou plusieurs *préparations* ne sont plus disponibles (Scénario ***Préparation indisponible***).
  - 3a.2 Renvoie à 3.  
   
- 10a. [Il manque une ou plusieurs *préparations* pour terminer une *partie de commande*]
  - 10a.1 La commande est en attente de la ou les *préparations* manquantes.
  - 10a.2 Renvoie à 1.
  
***Scénario d'exception :***  
- 2a. [Le système n'est pas connecté à internet]
  - 2a.1 Le système prévient le serveur qu'il ne parvient pas à se connecter à internet.
  - 2a.2 Le système met fin à la session.  
    
---

### Glossaire :

- *préparation* : Entrée / Plat / Dessert / Boisson
- *partie de la commande* : Ensemble des entrées, des plats, des desserts ou des boissons.
