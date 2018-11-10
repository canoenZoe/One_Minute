# Prendre une commande

---

**Nom du cas :** Prendre une commande  
**But :** Le serveur prend une commande à une table pour un client  
**Acteur principal :** Serveur  
**Date de création :** 06/11/2018  
**Nom du responsable de création :** Zoé Canoen  
**Dernière date de mise à jour :**  10/11/2018
**Nom du responsable de la dernière modification :**  Sami Barchid
**Version :** 1  

---

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

*Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".*

------

**Pré-conditions :**  

- Le serveur possède une tablette.
- Le serveur est authentifié sur sa tablette.
- Un client attend de passer commande.

**Déclenchement :**

Le serveur indique qu'il prend une commande.

**Scénario nominal :**  

1. Le serveur indique qu'il prend une commande.
2. Le système affiche la liste des tables disponibles.
2. Le serveur choisit le numéro de table du client.
3. Le système valide le numéro de table choisi.
4. Le système réserve la table pour le client.
5. Branchement au cas d'utilisation : "ajouter une préparation à la commande."

**Post-condition :**

- la table est réservée dans le système pour le client.
- La commande est enregistrée dans l'état "en cours".

**Scénario d'exception :**  
- 3.a.1 [Numéro de table incorect]
- 3.a.2.1 Le système retourne un message d'erreur.
- 3.a.2.2 Le système retourne à son état d'avant l'exécution du CU. 

- \*.a.1 [Panne (réseauxn système, etc)]
	- \*.a.1 Le système indique un message d'erreur fatale.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.

---

**Diagramme de séquence :**
