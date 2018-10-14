***Nom du cas :*** Préparation indisponible  
***But :*** Ce cas montre les étapes permettant au cuisinier de rendre *indisponible* une *préparation*.  
***Acteur principal :*** Le cuisinier    
***Date de création :*** 11/09/2018  
***Date de mise à jour :*** 14/10/2018  
***Nom du responsable :*** Laurine Drodzinski   
***Version :*** 2.0

---

***Pré-conditions :***  
Il n'y a plus assez d'ingrédients pour cuisiner un certain type de *préparation*.  
  
***Déclenchement :*** Le cas commence lorsque le cuisinier se rend compte qu'une *préparation* ne peut pas être cuisinée.   
  
***Scénario nominal :***  
1. Le cuisinier sélectionne la *préparation* en question pour la rendre indisponible.  
2. Le système notifie les serveurs qu'une *préparation* ne peut pas être réalisée.  
3. Le système bloque la possibilité de sélectionner cette *préparation* lors de la prise d'une commande.  

***Post-condition :*** La *préparation* reste indisponible tant qu'il n'y a pas eu réapprovisionnement.  
  
***Scénarios alternatifs :***  
- 1a. [Réapprovisionnement des ingrédients]
  - 1a.1 Le cuisinier indique que la *préparation* est de nouveau disponible.
  - 1a.2 Le système débloque la possibilité de sélectionner cette *préparation* lors de la prise d'une commande.
  - 1a.3 Fin du scénario.
 
***Scénario d'exception :***  
- 2a. [Le système n'est pas connecté à internet]
  - 2a.1 Le système prévient le cuisinier qu'il ne parvient pas à se connecter à internet.
  - 2a.2 Le système met fin à la session.  
    
---

### Glossaire :

- *préparation* : Entrée / Plat / Dessert / Boisson
