# Suivre une commande

------

**Nom du cas :** Suivre une commande  
**But :** Le serveur souhaite suivre l'état d'avancement d'une commande  
**Acteur principal :** Serveur  
**Date de création :** 11/09/2018  
**Nom du responsable de création :** Laurine DRODZINSKI  
**Dernière date de mise à jour :** 06/11/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.2

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Néant

**Déclenchement :** 

- Le serveur souhaite vérifier l'état d'avancement d'une commande

**Scénario nominal :** 

1. Début du scénario
2. Le serveur indique qu'il souhaite afficher la liste des commandes en cours
3. Le système affiche la liste des commandes en cours
4. Le serveur sélectionne la commande du client
5. Le système affiche le résumé et l'état d'avancement de chaque ***partie de la commande*** sélectionnée
6. Le serveur consulte la commande du client
7. Fin du scénario

**Post-condition :**

- Le serveur a consulté l'état d'avancement d'une commande. 

**Continuité du scénario :**

- Lorsqu'une ***partie de la commande*** est prête, le scénario ***Servir une commande*** peut se réaliser.
- Lorsque toutes les ***parties de la commande*** ont été servie, le scénario ***Paiement*** peut se réaliser.

**Scénarios alternatifs :**  

- Néant

**Scénario d'exception :**  

- 3.a. [ Aucune commande n'est en cours ]
  - 3.a.1 Le système affiche qu'aucune commande est en cours
  - 3.a.2 Fin du scénario

------

**Diagramme de séquence :**
