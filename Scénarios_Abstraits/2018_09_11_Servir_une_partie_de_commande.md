# Servir une partie de commande


***Nom du cas :*** Servir une partie de commande.
***But :*** Le serveur sert une partie de la commande d'un client qui a été préparée par un préparateur.
***Acteur principal :*** Le serveur    
***Date de création :*** 11/09/2018  
***Date de mise à jour :*** 14/10/2018  
***Nom du responsable :*** Sami Barchid
***Version :*** 2.0

---

***Pré-condition :***
- La partie de la commande à servir est prête.
- Le serveur possède une tablette.
- Le serveur est authentifié sur sa tablette.

***Déclenchement :*** Le serveur consulte les parties de commandes prêtes à servir.

***Post-condition :***
- La partie de commande est servie au client.
- Le client

***Scénario nominal :***
1. Le serveur consulte les parties de commandes prêtes à servir.
2. Le système affiche les parties de commandes prêtes à servir.
3. Le serveur sélectionne une partie de commande.
4. Le système enregistre la sélection du serveur.
5. Le système notifie la sélection du serveur en cuisine.
6. Le serveur va chercher la partie de commande à servir.
7. Le serveur sert la partie de commande au client.
8. Le serveur indique au système que la partie de commande est servie.
9. Le système notifie en cuisine la fin du service de la partie de commande.

***Scénarios alternatifs :***
- 2.a. [Aucune parties de commandes prêtes à servir]
	- Le système affiche un message d'erreur au serveur.
	- Retour à l'étape 1.

	***Post-condition :***
	- La partie de commande est servie au client.
	- Le client

***Scénarios d'exception :***
- 2.a. [Aucune partie de commande prête à servir]
	- Le système
- 4.a. [La partie de commande sélectionnée est annulée/terminée]
	- 4.a.1. Le système affiche un message d'erreur au serveur.
	- 4.a.2. Le système retourne à l'état d'avant le déclenchement.
- \*.a. [Panne de réseau]
	- Le système indique que le réseau a été coupé.
	- Le système retourne à son état d'avant le déclenchement.
