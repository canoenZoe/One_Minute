# Cuisiner une ***préparation***

------

**Nom du cas :** Cuisiner une ***préparation***  
**But :** Ce cas montre les étapes permettant au ***préparateur*** de s'occuper d'une ***préparation***  
**Acteur principal :** ***Préparateur***  
**Date de création :** 11/09/2018  
**Nom du responsable de création :** Laurine DRODZINSKI  
**Dernière date de mise à jour :** 08/11/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.3

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Le préparateur a prit en charge une préparation

**Déclenchement :** 

- Le ***préparateur*** souhaite s'occuper d'une ou plusieurs ***préparations*** 

**Scénario nominal :**  

1. Début du scénario
2. Le ***préparateur*** commence à préparer
3. Le ***préparateur*** termine la ***préparation***
4. Le ***préparateur*** indique au système qu'il a terminé les ***préparations***
5. Le ***préparateur*** indique qu'une ***partie de commande*** est terminée
6. Le système modifie l'état de la ***partie de commande*** terminée
7. Le système notifie les serveurs
8. Fin du scénario

**Continuité du scénario :**

-  Le scénario ***Servir une commande*** peut être réalisé.

**Post-condition :**

- Les serveurs sont notifiés afin qu'ils puissent servir une ***partie de commande***.

**Scénarios alternatifs :**  

- 2.a [La ***préparation*** ne peut être réalisée]
  - Réalisation du scénario ***Préparation indisponible***

**Scénario d'exception :**  

- Néant

