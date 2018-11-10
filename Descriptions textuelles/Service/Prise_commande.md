# Prise d'une commande

---

**Nom du cas :** Prise d'une commande  
**But :** Le serveur prend une commande à une table pour un client  
**Acteur principal :** Serveur  
**Date de création :** 06/11/2018  
**Nom du responsable de création :** Zoé Canoen  
**Dernière date de mise à jour :**  09/11/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.2

---

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Le client est assis à une table.

**Déclenchement :**

- Le client appelle le serveur pour prendre sa commande
- Le serveur décide d'aller prendre la commande d'une table

**Scénario nominal :**  

1. Début du scénario
2. Le serveur propose le menu au client (***Voir Proposer menu***)
3. Le serveur créé une nouvelle commande avec le numéro de table
4. Le serveur demande au client ce qu'il a choisi
5. Le client énonce les diverses préparations qu'il souhaite commander
6. Le serveur sélectionne les préparations parmis les préparations disponibles
7. Le serveur valide la commande
8. Fin du scénario

**Continuité du scénario :**

-

**Post-condition :**

- La commande est validée et est prête à être cuisinée

**Scénarios alternatifs :**  

- 6.a [Une des préparations énnoncées n'est plus disponible]
    - 6.a.1 Le serveur annonce que la préparation n'est plus disponible
    - 6.a.2 Le serveur invite le client à choisir une autre préparation
    - Reprise à l'étape 5

**Scénario d'exception :**  

- Néant

---

**Diagramme de séquence :**
