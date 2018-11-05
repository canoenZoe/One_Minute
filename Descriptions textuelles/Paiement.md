# Paiement d'une commande

------

**Nom du cas :** Paiement d'une commande
**But :** Le client souhaite régler l'addition de sa commande
**Acteur principal :** Serveur
**Date de création :** 19/10/2018
**Nom du responsable de création :** Anthony SLIMANI
**Dernière date de mise à jour : **31/10/2018
**Nom du responsable de la dernière modification :** Anthony SLIMANI
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**  

- Néant

**Déclenchement :** 

- Le client appelle le serveur pour demander à régler sa commande

**Scénario nominal :**  

1. Début du scénario
2. Le serveur recherche la commande du client à partir de son numéro de table
3. Le système affiche la commande
4. Le serveur choisit de ***générer l'addition***
5. Le système affiche l'addition de la commande du client
6. Le serveur indique que le réglement à bien été effectué
7. Le système change l'état de la commande à "Réglé"
8. Le système retire la commande de la liste des commandes en cours
9. Fin du scénario

**Post-condition :**

- Le commande est retiré de la liste des commandes en cours

**Scénarios alternatifs :**  

- 1.a[Le client n'est plus présent du restaurant]
  - 1.a.1 Le serveur annule la commande
  - 1.a.2 Le système change l'état de la commande à "Annulé"
  - Reprise à l'étape 7

**Scénario d'exception :**  

- 

------

### Glossaire :

- ***Générer l'addition*** : Récaptitulatif virtuel du détails de la commande du client avec le montant total de sa commande, celui-ci pourra être imprimé cf.*"Imprimer_facture.md"*

