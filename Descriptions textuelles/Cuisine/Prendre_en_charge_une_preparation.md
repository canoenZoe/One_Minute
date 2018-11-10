# Prendre en charge une ***préparation***

------

**Nom du cas :** Prendre en charge une ***préparation***  
**But :** Ce cas montre les étapes permettant au ***préparateur*** de s'occuper d'une préparation  
**Acteur principal :** Préparateur  
**Date de création :** 03/11/2018  
**Nom du responsable de création :** Zoé CANOEN  
**Dernière date de mise à jour :** 08/11/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.1  

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Des commandes sont en cours

**Déclenchement :** 

- Le ***préparateur*** souhaite s'occuper d'une ou plusieurs ***préparation.s***.

**Scénario nominal :**  

1. Début du scénario
2. Le ***préparateur*** sélectionne la liste des ***préparations*** non prises en charge
3. Le système affiche la liste des ***préparations*** à réaliser
4. Le ***préparateur*** choisit une ou plusieurs ***préparations*** qu'il s'apprête à préparer
5. Le ***préparateur*** sélectionne son nom dans la liste des ***préparateurs***
6. Le ***préparateur*** valide son choix
7. Le système réserve la ou les ***préparation.s*** choisie.s afin qu'aucun autre ***préparateur*** ne puisse les sélectionner
8. Fin du scénario

**Post-condition :**

- La ou les ***préparation.s*** choisie.s ne peuvent plus être pris en charge par d'autres ***préparateurs***

**Continuité du scénario :**

- Le scénario ***Cuisiner une préparation*** peut être réalisé.

**Scénarios alternatifs :**  

- Néant

**Scénario d'exception :**  

- 3.a [ Aucune ***préparation*** dans la liste des ***préparations*** à réaliser ]
  - 3.a.1 Le système affiche un message indiquant qu'aucune ***préparation*** n'est à réaliser
  - 3.a.2 Fin du scénario
- 7.a [ La ***préparation*** a été déjà été prise en charge ]
  - 7.a.1 Le système affiche un message indiquant que la ***préparation*** a été déjà été prise en charge
  - 7.a.2 Fin du scénario

------

**Diagramme de séquence :**



