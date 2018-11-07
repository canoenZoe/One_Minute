# Cuisiner une ***préparation***

------

**Nom du cas :** Cuisiner une ***préparation***
**But :** Ce cas montre les étapes permettant au ***préparateur*** de s'occuper d'une ***préparation***
**Acteur principal :** ***Préparateur***
**Date de création :** 11/09/2018
**Nom du responsable de création :** Laurine DRODZINSKI
**Dernière date de mise à jour : ** 06/11/2018
**Nom du responsable de la dernière modification :** Anthony SLIMANI
**Version :** 2.2

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Le préparetur a prit en charge une préparation

**Déclenchement :** 

- Le ***préparateur*** souhaite s'occuper d'une ou plusieurs ***préparations*** 

**Scénario nominal :**  

1. Début du scénario
2. Le ***préparateur*** commence a préparer
3. Le ***préparateur*** termine la ***préparation***
4. Le ***préparateur*** indique au système qu'il a terminé les ***préparations***
5. Le ***préparateur*** indique qu'une ***partie de commande*** est terminée
6. Le système notifie les serveurs
7. Fin du scénario

**Continuité du scénario :**

-  Le scénario ***Servir une commande*** peut être réalisé.

**Post-condition :**

- Les serveurs sont notifiés afin qu'ils puissent servir une ***partie de commande***.

**Scénarios alternatifs :**  

- 4a. [Il manque une ou plusieurs ***préparations*** pour terminer une *partie de commande*]
  - 4a.1 La commande est en attente de la ou les *préparations* manquantes.
  - 4a.2 Renvoie à 1.

**Scénario d'exception :**  

- 2a. [Le système n'est pas connecté à internet]
  - 2a.1 Le système prévient le cuisinier qu'il ne parvient pas à se connecter à internet.
  - 2a.2 Le système met fin à la session.  

------

**Diagramme de séquence :**