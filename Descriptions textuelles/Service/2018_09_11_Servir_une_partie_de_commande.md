# Servir une partie de commande

------

**Nom du cas :** Servir une partie de commande
**But :** Le serveur sert une partie de la commande d'un client qui a été préparée par un préparateur
**Acteur principal :** Serveur
**Date de création :** 11/09/2018
**Nom du responsable de création :**
**Dernière date de mise à jour :** 06/11/2018
**Nom du responsable de la dernière modification :** Anthony SLIMANI
**Version :** 2

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- La partie de la commande à servir est prête.

**Déclenchement :**

- Le serveur consulte les parties de commandes prêtes à servir.

**Scénario nominal :**  

1. Début du scénario
2. Le serveur consulte les parties de commandes prêtes à servir.
3. Le système affiche les parties de commandes prêtes à servir.
4. Le serveur sélectionne une partie de commande.
5. Le système enregistre la sélection du serveur.
6. Le système notifie la sélection du serveur en cuisine.
7. Le serveur va chercher la partie de commande à servir.
8. Le serveur sert la partie de commande au client.
9. Le serveur indique au système que la partie de commande est servie.
10. Le système notifie en cuisine la fin du service de la partie de commande.
11. Fin du scénario

**Post-condition :**

- La partie de commande est servie au client.

**Scénarios alternatifs :**  

- 2.a. [Aucune parties de commandes prêtes à servir]
  - Le système affiche un message d'erreur au serveur.
  - Retour à l'étape 1.

**Scénario d'exception :**  

- 2.a. [Aucune partie de commande prête à servir]
  - Le système
- 4.a. [La partie de commande sélectionnée est annulée/terminée]
  - 4.a.1. Le système affiche un message d'erreur au serveur.
  - 4.a.2. Le système retourne à l'état d'avant le déclenchement.
- \*.a. [Panne de réseau]
  - Le système indique que le réseau a été coupé.
  - Le système retourne à son état d'avant le déclenchement.

------

**Diagramme de séquence :**

-
