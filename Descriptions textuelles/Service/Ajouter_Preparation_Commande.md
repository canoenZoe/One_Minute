# Ajouter préparation dans une commande

---

**Nom du cas :** Ajouter une préparation à la commande  
**But :** Ajouter une préparation à une commande existante  
**Acteur principal :** Serveur  
**Date de création :** 06/11/2018  
**Nom du responsable de création :** Zoé Canoen  
**Dernière date de mise à jour :** 10/11/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.2

---

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Le client a déjà commandé une fois auparavant.  

**Déclenchement :** Le cas commence lorsque le client souhaite ajouter des ***préparations*** à sa commande.

**Scénario nominal :**  

1. Début du scénario
2. Le client fait appel à un serveur afin de changer sa commande.  
3. Le serveur arrive à la table du client.  
4. Le serveur prend son  ***outil de travail***.  
5. Le serveur sélectionne la liste des commandes en cours.  
6. Le système affiche la liste des commandes en cours.  
7. Le serveur sélectionne la commande du client.  
8. Le système affiche le résumé de la commande sélectionnée.  
9. Le serveur demande au client ce qu'il souhaite commander.
10. Le serveur ajoute la ou les nouvelles ***préparations*** à la commande.  
11. Le serveur confirme l'ajout de ***préparations***.  
12. Le système notifie l'équipe de ***préparateur*** que la commande a été modifiée.
13. Fin du scénario

**Post-condition :**
- L'équipe de cuisine est notifiée de la modification de la commande en question.  

**Scénarios alternatifs :**
- 3.a. [Aucun serveur n'est disponible]
  - 3.a.1 Le client attend qu'un serveur soit de nouveau disponible.
  - 3.a.2 Retour à l'étape 2.

- 10a. [Une ou plusieurs ***préparations*** demandées ne sont plus disponibles]
  - 10.a.1 Le système affiche que la ou les *préparations* ne sont plus disponibles.
  - 10.a.2 Le serveur ne peut pas les sélectionner.
  - 10.a.3 Retour à l'étape 9.

**Scénario d'exception :**
- Néant

------

**Diagramme de séquence :**

