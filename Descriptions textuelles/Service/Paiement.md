# Paiement d'une commande

------

**Nom du cas :** Paiement d'une commande  
**But :** Le client souhaite régler l'addition de sa commande  
**Acteur principal :** Serveur  
**Date de création :** 19/10/2018  
**Nom du responsable de création :** Anthony SLIMANI  
**Dernière date de mise à jour :** 06/11/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.2

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Le serveur consulte le suivi de la commande
- L'état de réglementation de la commande est à *"Non réglé"*

**Déclenchement :** 

- Le client appelle le serveur pour demander à régler sa commande

**Scénario nominal :**  

1. Début du scénario
2. Le serveur choisit de ***générer l'addition***
3. Le système affiche l'addition de la commande du client
4. Le serveur saisit le montant de la commande sur le système de paiement
5. Le client paie sa commande
6. Le serveur indique au système que le réglement a bien été effectué
7. Le système change l'état de réglementation de la commande à *"Réglé"*
8. Le système retire la commande de la liste des commandes en cours
9. Fin du scénario

**Post-condition :**

- L'état de réglementation de la commande est à *"Réglé"*

**Continuité du scénario :**

- Si le client le souhaite, il peut demander au serveur le détail de sa commande sous forme physique. Le scénario ***Imprimer l'addition d'une commande*** peut se réaliser.

**Scénarios alternatifs :**  

- 5.a [ Le paiement du client est refusé ]

**Scénario d'exception :**  

- 1.a [ Le client n'est plus présent au restaurant ]
  - 1.a.1 Le serveur annule la commande
  - 1.a.2 Le système change l'état de la commande à *"Fini"*
  - 1.a.3 Fin du scénario

------

**Diagramme de séquence :**
