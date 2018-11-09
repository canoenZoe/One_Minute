# Servir une partie de commande

------

**Nom du cas :** Servir une partie de commande  
**But :** Le serveur sert une partie de la commande d'un client qui a été préparée par un préparateur  
**Acteur principal :** Serveur  
**Date de création :** 11/09/2018  
**Nom du responsable de création :** Sami BARCHID  
**Dernière date de mise à jour :** 09/11/2018  
**Nom du responsable de la dernière modification :** Zoé Canoen  
**Version :** 2

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- La partie de la commande à servir est prête.
- Un cuisinier à terminer une ***partie de commande***, voir scénario "Cuisiner une préparation"

**Déclenchement :**

- Le serveur consulte les parties de commandes prêtes à servir.

**Scénario nominal :**  

1. Début du scénario
2. Le serveur consulte les parties de commandes prêtes à servir.
3. Le système affiche les parties de commandes prêtes à servir.
4. Le serveur sélectionne une partie de commande.
5. Le système supprime la partie de commande dans la liste des commandes à servir.
7. Le serveur va chercher la partie de commande à servir.
8. Le serveur sert la partie de commande au client.
11. Fin du scénario

**Post-condition :**

- La partie de commande est servie au client.

**Remarque :**
- Le serveur a reçu une notification de la cuisine avant le sénario. Il n'est pas obligé d'y répondre directement sans faire attention à la notification.
 C'est pour cela que nous ne mettons pas cela en post condition.

**Scénarios alternatifs :**  

- 2.a. [Aucune parties de commandes prêtes à servir]
    - Rien ne se passe.

**Scénario d'exception :**  

- 4.a. [La partie de commande sélectionnée est annulée/terminée]
  - 4.a.1. Le système affiche un message d'erreur au serveur.
  - 4.a.2. Le système retourne à l'état "afficher les parties de commandes".
- \*.a. [Panne de réseau]
  - Le système indique que le réseau a été coupé.
  - Le système retourne à son état d'avant le déclenchement.

------

**Diagramme de séquence :**

-
