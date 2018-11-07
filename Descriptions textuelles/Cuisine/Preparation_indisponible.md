# Préparation indisponible

------

**Nom du cas :** ***Préparation*** indisponible
**But :** Ce cas montre les étapes permettant au ***préparateur*** de rendre ***indisponible*** une préparation
**Acteur principal :** Préparateur
**Date de création :** 11/09/2018
**Nom du responsable de création :** Laurine DRODZINSKI
**Dernière date de mise à jour : **06/11/2018
**Nom du responsable de la dernière modification :** Anthony SLIMANI
**Version :** 2.2

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Il n'y a plus assez d'ingrédients pour cuisiner un certain type de ***préparation***.  

**Déclenchement :** 

- Le cas commence lorsque le cuisinier se rend compte qu'une ***préparation*** ne peut pas être cuisinée. 

**Scénario nominal :**  

1. Début du scénario
2. Le cuisinier sélectionne la ***préparation*** en question pour la rendre indisponible.  
3. Le système notifie les serveurs qu'une ***préparation*** ne peut pas être réalisée.  
4. Le système bloque la possibilité de sélectionner cette ***préparation*** lors de la prise d'une commande.
5. Fin du scénario

**Post-condition :**

- La ***préparation*** reste indisponible tant qu'il n'y a pas eu réapprovisionnement.  

**Scénarios alternatifs :**  

- 1.a [Réapprovisionnement des ingrédients]
  - 1a.1 Le cuisinier indique que la *préparation* est de nouveau disponible.
  - 1a.2 Le système débloque la possibilité de sélectionner cette *préparation* lors de la prise d'une commande.
  - 1a.3 Fin du scénario.

**Scénario d'exception :**  

- 2.a [Le système n'est pas connecté à internet]
  - 2.a.1 Le système prévient le cuisinier qu'il ne parvient pas à se connecter à internet.
  - 2.a.2 Le système met fin à la session.  

------

**Diagramme de séquence :**



