***Nom du cas :*** Suivre une commande  
***But :*** Ce cas montre les étapes permettant au serveur de suivre l'état d'avancement d'une commande.  
***Acteur principal :*** Le serveur   
***Date de création :*** 11/09/2018  
***Date de mise à jour :*** 14/10/2018  
***Nom du responsable :*** Laurine Drodzinski   
***Version :*** 2.0

---

***Pré-conditions :***  
Des commandes sont en cours.  
Le serveur est authentifié dans le système.  
  
***Déclenchement :*** Le cas commence lorsque le serveur souhaite vérifier l'état d'avancement d'une commande.   
  
***Scénario nominal :***  
1. Le serveur veut savoir si la *préparation* d'un client est prête.  
2. Le serveur sélectionne la liste des commandes en cours.  
3. Le système affiche la liste des commandes en cours.  
4. Le serveur sélectionne la commande du client. 
5. Le système affiche le résumé et l'état d'avancement de la commande sélectionnée.  
6. Le serveur voit quelles sont les parties de la commande qui sont prêtes ou non.  
  
*Remarque :* Lorsqu'une partie de la commande est prête, elle peut alors être servie. Le scénario ***Servir une commande*** peut se réaliser.    
  
***Post-condition :*** Le serveur a consulté l'état d'avancement d'une commande.  
  
***Scénario d'exception :***  
- 2a. [Le système n'est pas connecté à internet]
  - 2a.1 Le système prévient le serveur qu'il ne parvient pas à se connecter à internet.
  - 2a.2 Le système met fin à la session.  
    
---

### Glossaire :

- *préparation* : Entrée / Plat / Dessert / Boisson
