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

 
 
 <details><summary>1. ##### Ajout d'un plat dans une commande</summary>
<p>

Ajouter un plat dans une commande déjà en cours.


</p>
</details>


 2. ##### Établir un menu
Créer ou modifier la carte de restaurant.

 3. ##### Le client prend sa commande
Un client prend commande en interagissant avec le système.

 4. ##### Paiement
Le client a terminé son repas et veut payer l'addition.

 5. ##### Plat indisponible
Un plat n'est plus disponible pour la clientèle et il faut le notifier à tous.

 6. ##### Prendre une commande
Un serveur prend la commande pour des clients.

 7. ##### Servir une commande
Une partie de la commande est prête à être envoyée au client.

 8. ##### Suivre une commande
Un membre du personnel veut suivre l'état d'avancement des commandes.

 9. ##### Cuisiner un plat
Un cuisinier veut préparer un plat pour un client 

----------------------------------------------------------------

## Ajouts de plats dans une commande

#### Description :

***Alice*** peut ajouter des plats dans une commande déjà en cours si ***Bob*** le désire.

#### Scénario :

- ***Bob*** veut ajouter un plat à sa commande en cours.
- ***Bob*** appelle ***Alice*** pour changer sa commande.
  - ***Alice*** n'est pas disponible.
- ***Alice*** prend sa tablette.
- ***Alice*** ajoute le nouveau plat à la commande.
  - Le plat n'est plus disponible.
- L'équipe de cuisine est avertie de l'ajout.
  - Problème de notification si problème de connexion à internet.

#### Glossaire :

- ***Bob*** : client
- ***Alice*** : serveuse

----------------------------------------------------------------

## Etablir un menu

#### Description :

***Albert*** crée ou modifie la carte du restaurant, avant l'ouverture ou après la fermeture du restaurant.

#### Scénario :

- ***Albert*** commence à créer ou modifier la carte dans l'application.
- ***Albert*** crée ou modifie divers éléments.
- ***Albert*** termine la création ou la modification.
- La carte s'actualise sur les diverses tablettes.
    - Problème d'actualisation si les tablettes ne sont pas connectées à internet.

#### Glossaire :

- ***Albert*** : patron

----------------------------------------------------------------

## Le client prend sa commande

*La fonctionnalité étant optionnelle, elle sera décrite et travaillée ultérieurement. Nous la prévoyons pour la V2, voir V3. Nous ferons néanmois le nécéssaire pour pouvoir garder l'application la plus généraliste possible pour pouvoir incorporer cette fonctionnalité plus tard.*

----------------------------------------------------------------

## Paiement

#### Description :

- ***Bob*** a fini de manger et souhaite quitter le restaurant mais avant il doit régler ***l'addition*** de sa commande

#### Scénario :

- ***Bob*** demande ***l'addition*** à ***Alice***
  - ***Alice*** n'est pas disponible
- ***Alice*** recherche ***l'addition*** à partir du numéro de table de ***Bob*** par l'intermédaire de l'application
  - ***Alice*** n'a pas accès au service de commande sur l'application
- L'application affiche ***l'addition***
- ***Alice*** informe le montant de ***l'addition*** à ***Bob***
- ***Bob*** paie ***l'addition*** par le moyen de paiement choisi
- ***Alice*** indique à l'application que ***l'addition*** a bien été réglé
- L'application archive la commande de ***Bob***

#### Questions :

- Faut-il générer ***l'addition*** de manière physique à ***Bob*** ?
  - ***L'addition*** a besoin d'être généré de manière physique notamment pour les notes de frais

#### Glossaire :

- ***L'addition*** : facture de la commande indiquant la liste des plats commandés ainsi que le montant total de la commande
- ***Bob*** : client
- ***Alice*** : serveuse

----------------------------------------------------------------

## Plat indisponible

#### Description :

- ***Roger*** s'aperçoit que la réalisation d'un plat ne peut être réalisé et doit donc rendre ***indisponible*** ce plat.

#### Scénario :

- ***Roger*** indique que le plat est ***indisponible*** sur l'application
  - Des commandes comprenant ce plat sont en cours
    - L'application annule les commandes comportant ce plat
    - L'application notifie les serveurs des commandes annulées
- L'application bloque la possibilité de sélectionner ce plat lors d'une commande

[En attente de ***réapprovisionnement*** de.s ingrédient.s]_
- ***Roger*** indique que le plat est de nouveau disponible
- L'application débloque la possibilité de sélectionner ce plat lors d'une commande

#### Glossaire :

- ***Roger*** : cuisinier
- ***indisponible*** : le plat ne peut être réalisé par manque de un ou plusieurs ingrédient.s le constituant.
- ***réapprovisionnement*** : Action de recevoir un nouvel apport de marchandises afin de renouveler les stocks.

----------------------------------------------------------------

## Prendre une commande

#### Description :

***Alice*** propose à ***Bob*** de prendre sa première commande.

#### Scénario :

- ***Alice*** propose le menu à ***Bob***.
- ***Bob*** choisit ce qu'il souhaite commander.
- ***Alice***, à partir de sa tablette, transmet la commande et le numéro de table aux cuisiniers.
- Les cuisiniers sont au courant de la commande.

#### Glossaire :

- ***Bob*** : client
- ***Alice*** : serveuse

----------------------------------------------------------------

## Servir une commande

#### Description :

Lorsque qu'une ***partie de la commande*** est prête, il faut la servir à Bob.

#### Scénario :

- ***Alice*** est mise au courant qu'une ***partie de la commande*** est prête.
  - Problème de notification si problème de connexion à internet.
- ***Alice*** indique sur l'application qu'elle va la chercher.
- ***Alice*** récupère la ***partie de la commande***.
- ***Alice*** la ramène à Bob.

#### Glossaire :

- ***Bob*** : client
- ***Alice*** : serveuse
- ***partie de la commande*** : pack de boissons, de plats ou de desserts

----------------------------------------------------------------

## Suivre une commande

#### Description :

Le personnel du restaurant peut suivre l'état d'avancement d'une commande en cours ou passée.

#### Scénario :

- **Bob** veut savoir si la commande de spaghetti de **Alice** est prête.
- **Bob** sélectionne la commande de **Alice** pour voir son état.
- **Bob** voit que les spaghettis de **Alice** sont prêts.
- **Bob** voit que son mojito fraise n'est pas prêt.
- **Bob** va chercher les spaghettis en cuisine.
- **Bob** amène les spaghettis à **Alice**.
- **Bob** indique que les spaghettis sont servis.

#### Glossaire :

- **Bob** : serveur
- **Alice** : cliente
- **Spaghettis** : partie de la commande de Alice.
- **État** : état d'avancement de la commande.

----------------------------------------------------------------

## Cuisiner un plat

#### Description :

***Roger*** désire faire un plat, et doit informer l'application sur quel(s) plat(s) il est en train de cuisiner.

#### Scénario :

- ***Roger*** veut cuisiner un (ou plusieurs) plat(s).
- ***Roger*** valide son identité pour voir les plats qui lui sont assignés.
- ***Roger*** choisi un (ou plusieurs) plat(s) qu'il s'apprete à cuisinier. 
- ***Roger*** valide et peut commencer à cuisiner.
- Une fois que ***Roger*** a terminé son plat, il s'identifie à nouveau pour dire qu'il a terminé un plat.
- Ensuite, SOIT 
    * son plat permet de terminer une ***partie de la commande***, 
      dans ce cas une notification est envoyée aux serveurs pour venir chercher le plat.
    * il manque un plat pour la commande, la commande est alors en attente du plat manquant. 
      Et attend qu'un cuisinier cuisine le plat manquant.

#### Glossaire :

- ***Roger*** : cuisinier
- ***partie de la commande*** : pack de boissons, de plats ou de desserts etc.

----------------------------------------------------------------

## Diagrammes de CU


## Diagramme des classe


