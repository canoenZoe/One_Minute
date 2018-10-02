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

 1. #### Ajout d'un plat dans une commande
Ajouter un plat dans une commande déjà en cours.


 2. #### Établir un menu
Créer ou modifier la carte de restaurant.

 3. #### Le client prend sa commande
Un client prend commande en interagissant avec le système.

 4. #### Paiement
Le client a terminé son repas et veut payer l'addition.

 5. #### Plat indisponible
Un plat n'est plus disponible pour la clientèle et il faut le notifier à tous.

 6. ##### Prendre une commande
Un serveur prend la commande pour des clients.

 7. ##### Servir une commande
Une partie de la commande est prête à être envoyée au client.

 8. ##### Suivre une commande
Un membre du personnel veut suivre l'état d'avancement des commandes.

 9. ##### Cuisiner un plat
Un cuisinier veut préparer un plat pour un client


 ### Les scénarios : La description

 <details><summary>Les acteurs</summary>

<p>

- ***Bob*** : client
- ***Alice*** : serveuse
- ***Roger*** : cuisinier
- ***Albert*** : patron

</p>

</details>


 <details><summary>1. Ajout d'un plat dans une commande</summary>

<p>

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

----------------------------------------------------------------
</p>
</details>

 <details><summary>2. Etablir un menu</summary>

<p>

## Etablir un menu

#### Description :

***Albert*** crée ou modifie la carte du restaurant, avant l'ouverture ou après la fermeture du restaurant.

#### Scénario :

- ***Albert*** commence à créer ou modifier la carte dans l'application.
- ***Albert*** crée ou modifie divers éléments.
- ***Albert*** termine la création ou la modification.
- La carte s'actualise sur les diverses tablettes.
    - Problème d'actualisation si les tablettes ne sont pas connectées à internet.

----------------------------------------------------------------
</p>
</details>

 <details><summary>3. Le client prend sa commande</summary>

<p>

## Le client prend sa commande

*La fonctionnalité étant optionnelle, elle sera décrite et travaillée ultérieurement. Nous la prévoyons pour la V2, voir V3. Nous ferons néanmois le nécéssaire pour pouvoir garder l'application la plus généraliste possible pour pouvoir incorporer cette fonctionnalité plus tard.*

----------------------------------------------------------------
</p>
</details>

 <details><summary>4. Paiement</summary>

<p>

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

----------------------------------------------------------------
</p>
</details>

 <details><summary>5. Plat indisponible</summary>

<p>

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

----------------------------------------------------------------
</p>
</details>

 <details><summary>6. Prendre une commande</summary>

<p>

## Prendre une commande

#### Description :

***Alice*** propose à ***Bob*** de prendre sa première commande.

#### Scénario :

- ***Alice*** propose le menu à ***Bob***.
- ***Bob*** choisit ce qu'il souhaite commander.
- ***Alice***, à partir de sa tablette, transmet la commande et le numéro de table aux cuisiniers.
- Les cuisiniers sont au courant de la commande.

----------------------------------------------------------------
</p>
</details>

 <details><summary>7. Servir une commande</summary>

<p>

## Servir une commande

#### Description :

Lorsque qu'une ***partie de la commande*** est prête, il faut la servir à Bob.

#### Scénario :

- ***Alice*** est mise au courant qu'une ***partie de la commande*** est prête.
  - Problème de notification si problème de connexion à internet.
- ***Alice*** indique sur l'application qu'elle va la chercher.
- ***Alice*** récupère la ***partie de la commande***.
- ***Alice*** la ramène à Bob.

----------------------------------------------------------------
</p>
</details>

 <details><summary>8. Suivre une commande</summary>

<p>

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

----------------------------------------------------------------
</p>
</details>

 <details><summary>9. Cuisiner un plat</summary>

<p>

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

----------------------------------------------------------------
</p>
</details>

## Glossaire métier

- ***Addition*** : facture de la commande indiquant la liste des plats commandés ainsi que le montant total de la commande
- ***Commande*** : Note qui sert à savoir ce que le client a choisi. Elle est prise part un serveur, et est transmise aux cuisines.
- ***État*** : état d'avancement de la commande.
- ***Indisponible*** : Etat d'un plat qui ne peut pas/plus être réalisé par manque de un (ou plusieurs) ingrédient(s) le constituant.
- ***Partie de la commande*** : pack de boissons, de plats ou de desserts etc.
- ***Réapprovisionnement*** : Action de recevoir un nouvel apport de marchandises afin de renouveler les stocks.
- ***Stock*** : Ingrédients disponibles pour préparer les commandes.

## Diagrammes de CU

### Acteurs

Description des acteurs de l'application. Il est important de noter que les cuisiniers sont des préparateurs. Nous voulons faire quelque chose de généraliste, pour mettre dans la même classe le barman, le glacier, les cuisiniers...  

![GitHub Logo](/images/UC-Acteurs.png)

Nous avons choisi de représenter ces acteurs en fonction du sujet. Nous avons bien conscience que dans certains restaurants, il n'y a pas forcément de barman, mais plutôt des serveurs comme préparateurs. De plus dans les restaurants, il y a souvent des managers, comme dans la restauration rapide par exemple. 

#### Membre du restaurant

- Cet acteur est la généralisation des acteurs suivants :

#### Patron

- Gérant du restaurant.
- Possède un compte particulier qui lui permet de :
    - créer de nouveaux menus
    - modifier des menus existants
    - superviser l'état global du restaurant (avancement des commandes etc.)
- Doit être connecté à internet.

#### Serveur

- Est en contact avec les clients.
- Possède une tablette lui permettant de :
    - proposer le menu aux clients
    - prendre des commandes
    - suivre l'avancement des commandes    
    - générer l'addition et valider le paiement
- Doit être connecté à internet.

#### Préparateur

- Peut être un barman, un glacier, ou simplement un cuisinier etc.
- Ne possède pas une tablette à lui seul (une tablette pour les cuisiniers, une pour les barmans, glaciers etc.).
- Celle-ci lui permet de prendre en charge une préparation et également de gérer la disponibilité des plats.
- Doit être connecté à internet.


### Service

![GitHub Logo](/images/UC-Service.png)

Les serveurs a la possibilité de proposer le menu au client. Il pourra notamment prendre la commande de celui-ci. Pour celà, il devra saisir le numéro de table ainsi que d'ajouter une ou plusieurs préparations à la commande. Lorsque'une préparation est ajoutée dans une commande, les préparateurs sont directement notifiés. Les serveurs ont également la possibilité de servir une partie de la commande dès lors qu'ils ont été notifiés par les préparateurs. Il pourra également suivre l'état d'avancement de la commande. Dès que celle-ci est fini, le serveur pourra générer l'addiction puis d'indiquer si le réglement a bien été réalisé.

### Cuisine

![GitHub Logo](/images/UC-Cuisine.png)


Les préparateurs ont la possibilité d'indiquer sur l'application la prise en charge d'une préparation. Dès lors qu'il aura fini, il devra indiquer l'accomplissement de cette dernière. Cela aura comme conséquence de notifier tout les seveurs. Il a également la possibilité d'indiquer qu'une préparation est indisponible.


### Gérer le menu

![GitHub Logo](/images/UC-Menu.png)

Le patron a la possibilité de gérer le menu, c'est-à-dire d'ajouter, de modifier et de supprimer une préparation d'un menu.


## Diagramme de package

![GitHub Logo](/images/diagramme_packages.PNG)

## Diagramme de classes

![GitHub Logo](/images/diagramme_classe.PNG)

## Les premières versions des maquettes

Ces maquettes seront amenées à changer, c'est juste notre première version. Nous souhaitons laisser à tout le monde la possibilité de voir les différentes parties de l'application. A priori, les accès seront donnés par des managers. Le mieux sera de le faire en début de chaque jour, avant le service.

Le but de l'application est de gagner du temps. Notre application ne doit donc ne pas surcharger la charge de travail des cuisiniers. Nous ne connaissons pas le nombre de tablettes disponibles pour le restaurant, nous en comptons une par serveur pour le moment, et une ou deux en cuisine. Il sera tout à fait possible d'en mettre moins, car nous sommes bien conscients que le prix d'une tablette est assez cher. Cela pose pourtant certains problèmes, en effet, les cuisiniers ne doivent pas perdre de temps en se connectant. C'est pourquoi, nous vous proposons d'utiliser notre application avec un seul compte pour la cuisine. Chaque cuisinier doit juste d'identifier en cliquant sur un bouton avec leur nom pour que l'on sache que c'est eux qui ont fait cela. Cela leur permet de ne pas avoir à rentrer leur mot de passe. 

**Maquette de la partie cuisine**

![GitHub Logo](/Maquettes/Cuisine.png)

**Maquette de la partie service**

![GitHub Logo](/Maquettes/Service.png)

