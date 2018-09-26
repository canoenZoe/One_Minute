# Rapport final

## Auteurs 

* Anthony Slimani
* Laurine Drodzinski
* Noura Mares 
* Sami Barchid
* Zoé Canoen

## Résumé du problème 

Informatiser le processus de gestion des commandes d'un restaurant.
L'application doit permettre de prendre en charge une commande à partir
de la demande du client jusqu'au règlement de l'addition en passant par le traitement en cuisine.

## Les scénarios 

### Liste des scénarios

 1. ### Ajout d'un plat dans une commande
Ajouter un plat dans une commande déjà en cours.

 2. ### Établir un menu
Créer ou modifier la carte de restaurant.

 3. ### Le client prend sa commande
Un client prend commande en interagissant avec le système.

 4. ### Paiement
Le client a terminé son repas et veut payer l'addition.

 5. ### Plat indisponible
Un plat n'est plus disponible pour la clientèle et il faut le notifier à tous.

 6. ### Prendre une commande
Un serveur prend la commande pour des clients.

 7. ### Servir une commande
Une partie de la commande est prête à être envoyée au client.

 8. ### Suivre une commande
Un membre du personnel veut suivre l'état d'avancement des commandes.

 9. ### Cuisiner un plat
Un cuisinier veut préparer un plat pour un client 


### Ajouts de plats dans une commande

---

#### Description :

***Alice*** peut ajouter des plats dans une commande déjà en cours si ***Bob*** le désire.

---

#### Scénario :

- ***Bob*** veut ajouter un plat à sa commande en cours.
- ***Bob*** appelle ***Alice*** pour changer sa commande.
  - ***Alice*** n'est pas disponible.
- ***Alice*** prend sa tablette.
- ***Alice*** ajoute le nouveau plat à la commande.
  - Le plat n'est plus disponible.
- L'équipe de cuisine est avertie de l'ajout.
  - Problème de notification si problème de connexion à internet.

---

#### Glossaire :

- ***Bob*** : client
- ***Alice*** : serveuse

# Etablir un menu

---

### Description :

***Albert*** crée ou modifie la carte du restaurant, avant l'ouverture ou après la fermeture du restaurant.

---

### Scénario :

- ***Albert*** commence à créer ou modifier la carte dans l'application.
- ***Albert*** crée ou modifie divers éléments.
- ***Albert*** termine la création ou la modification.
- La carte s'actualise sur les diverses tablettes.
    - Problème d'actualisation si les tablettes ne sont pas connectées à internet.

---

### Glossaire :

- ***Albert*** : patron


### Prendre une commande

---

#### Description :

***Alice*** propose à ***Bob*** de prendre sa première commande.

---

#### Scénario :

- ***Alice*** propose le menu à ***Bob***.
- ***Bob*** choisit ce qu'il souhaite commander.
- ***Alice***, à partir de sa tablette, transmet la commande et le numéro de table aux cuisiniers.
- Les cuisiniers sont au courant de la commande.

---

#### Glossaire :

- ***Bob*** : client
- ***Alice*** : serveuse

## Diagrammes de CU


## Diagramme des classe


