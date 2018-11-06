***Nom du cas :*** Cuisiner une préparation  
***But :*** Ce cas montre les étapes permettant au cuisinier de s'occuper d'une préparation.
***Acteur principal :*** Le cuisinier    
***Date de création :*** 11/09/2018  
***Date de mise à jour :*** 14/10/2018  
***Nom du responsable :*** Laurine Drodzinski   
***Version :*** 2.0

---

***Pré-conditions :***  
Le cuisinier a prit en charge une préparation

***Déclenchement :*** Le cas commence lorsque le cuisinier souhaite souhaite s'occuper d'une ou plusieurs *préparations*.   

***Scénario nominal :***  
1. Le cuisinier commence a cuisiner.  
2. Le cuisinier termine la ou les *préparations*.
3. Le cuisinier indique au système qu'il a terminé les *préparations*.
4. Le cuisinier indique au système qu'une *partie de commande* est terminée.

***Post-condition :*** Les serveurs sont notifiés afin qu'ils puissent servir une *partie de commande*. Le scénario ***Servir une commande*** peut être réalisé.

***Scénarios alternatifs :***  

- 4a. [Il manque une ou plusieurs *préparations* pour terminer une *partie de commande*]
  - 4a.1 La commande est en attente de la ou les *préparations* manquantes.
  - 4a.2 Renvoie à 1.

***Scénario d'exception :***  
- 2a. [Le système n'est pas connecté à internet]
  - 2a.1 Le système prévient le cuisinier qu'il ne parvient pas à se connecter à internet.
  - 2a.2 Le système met fin à la session.  

---

### Glossaire :

- *préparation* : Entrée / Plat / Dessert / Boisson
- *partie de la commande* : Ensemble des entrées, des plats, des desserts ou des boissons.
