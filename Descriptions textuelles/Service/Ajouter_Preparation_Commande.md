# Ajouter préparation dans une commande

---

**Nom du cas :** Ajouter une préparation à la commande  
**But :** Ajouter une préparation à une commande existante ou non-existante  
**Acteur principal :** Serveur  
**Date de création :** 06/11/2018  
**Nom du responsable de création :** Zoé Canoen  
**Dernière date de mise à jour :** 06/12/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.3

---

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**
- Néant

**Déclenchement :** 

- Le cas commence lorsque le client souhaite ajouter des ***préparations*** à sa commande.

**Scénario nominal :**  

1. Début du scénario
2. Le serveur demande au client ce qu'il souhaite commander.
3. Le serveur ajoute la ou les nouvelles ***préparations*** à la commande.  
4. Le système ajoute la ou les nouvelles ***préparations*** à la commande.
5. Le système actualise l'affichage de la commande
6. Le serveur envoie la commande aux lieux de préparations
7. Le système enregistre la commande
8. Le système notifie l'équipe des ***préparateurs*** que la commande a été créée / modifiée.
9. Le système affiche une message de confirmation d'envoi
10. Fin du scénario

**Post-condition :**
- L'équipe de cuisine est notifiée de la modification de la commande en question.  

**Scénarios alternatifs :**
- 1.a. [La commande existe]
  - 1.a.1 Application du scénario ***Recherche d'une commande***
  - 1.a.2 Retour à l'étape 2.

- 3.a. [Une ou plusieurs ***préparations*** demandées ne sont plus disponibles]
  - 3.a.1 Le système affiche que la ou les ***préparations*** ne sont plus disponibles.
  - 3.a.2 Le serveur indique au client que la ou les ***préparations*** ne sont plus disponibles.
  - 3.a.3 Retour à l'étape 2.

**Scénario d'exception :**

- Néant


