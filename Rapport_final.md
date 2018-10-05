# Rapport final

## Auteurs

* Anthony Slimani
* Laurine Drodzinski
* Noura Mares
* Sami Barchid
* Zoé Canoen

## Introduction

Ce document récapitule la conception du projet de l'application "One Minute". Le but de cette application est de faire gagner du temps au restaurant. Nous nous sommes mis à la place de tous les acteurs du restaurant, mais d'avantage sur la partie service, cuisine et menu du restaurant. 

## Sommaire

1) Résumé du problème
2) Scénarios
3) Glossaire métier
4) Diagrammes de cas d'utilisation
5) Diagrammes de classes
6) Premières maquettes de l'application

## Résumé du problème

Le but de notre projet est d'informatiser le processus de gestion des commandes d'un restaurant.
L'application doit permettre de prendre en charge une commande à partir de la demande du client jusqu'au règlement de l'addition en passant par le traitement en cuisine.

## Scénarios

### Liste des scénarios

 1. #### Ajout d'une préparation dans une commande
Ajouter une préparation dans une commande déjà en cours.

 2. #### Établir un menu
Créer ou modifier la carte de restaurant.

 3. #### Le client prend sa commande
Un client prend commande en interagissant avec le système.

 4. #### Paiement
Le client a terminé son repas et veut payer l'addition.

 5. #### Préparation indisponible
Une préparation n'est plus disponible pour la clientèle et il faut le notifier à tous.

 6. ##### Prendre une commande
Un serveur prend la commande pour des clients.

 7. ##### Servir une commande
Une partie de la commande est prête à être envoyée au client.

 8. ##### Suivre une commande
Un membre du personnel veut suivre l'état d'avancement des commandes.

 9. ##### Cuisiner une préparation
Un cuisinier veut préparer une préparation pour un client.


 ### Description des scénarios

 <details><summary>Les acteurs</summary>

<p>

- ***Bob*** : client
- ***Alice*** : serveuse
- ***Roger*** : cuisinier
- ***Albert*** : patron

</p>

</details>


 <details><summary>1. Ajout d'une préparation dans une commande</summary>

<p>

----------------------------------------------------------------

## Ajouts de préparations dans une commande

#### Description :

***Alice*** peut ajouter des préparations dans une commande déjà en cours si ***Bob*** le désire.

#### Scénario :

- ***Bob*** veut ajouter une préparation à sa commande en cours.
- ***Bob*** appelle ***Alice*** pour changer sa commande.
  - ***Alice*** n'est pas disponible.
- ***Alice*** prend sa tablette.
- ***Alice*** ajoute la nouvelle préparation à la commande.
  - La préparation n'est plus disponible.
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

*La fonctionnalité étant optionnelle, elle sera décrite et travaillée ultérieurement. Nous la prévoyons pour la V2, voir V3. Nous ferons néanmoins le nécéssaire pour pouvoir garder l'application la plus généraliste possible pour pouvoir incorporer cette fonctionnalité plus tard.*

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

 <details><summary>5. Préparation indisponible</summary>

<p>

## Préparation indisponible

#### Description :

- ***Roger*** s'aperçoit que la réalisation d'une préparation ne peut être réalisée et doit donc rendre ***indisponible*** cette préparation.

#### Scénario :

- ***Roger*** indique que la préparation est ***indisponible*** sur l'application
  - Des commandes comprenant cette préparation sont en cours
    - L'application annule les commandes comportant cette préparation
    - L'application notifie les serveurs des commandes annulées
- L'application bloque la possibilité de sélectionner cette préparation lors d'une commande

[En attente de ***réapprovisionnement*** de.s ingrédient.s]_
- ***Roger*** indique que la préparation est de nouveau disponible
- L'application débloque la possibilité de sélectionner cette préparation lors d'une commande

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

## Cuisiner une préparation

#### Description :

***Roger*** désire faire une préparation, et doit informer l'application sur quelle(s) préparation(s) il est en train de cuisiner.

#### Scénario :

- ***Roger*** veut cuisiner une (ou plusieurs) préparation(s).
- ***Roger*** valide son identité pour voir les préparations qui lui sont assignées.
- ***Roger*** choisi une (ou plusieurs) préparation(s) qu'il s'apprête à cuisiner.
- ***Roger*** valide et peut commencer à cuisiner.
- Une fois que ***Roger*** a terminé sa préparation, il s'identifie à nouveau pour dire qu'il a terminé une préparation.
- Ensuite, SOIT
    * sa préparation permet de terminer une ***partie de la commande***,
      dans ce cas une notification est envoyée aux serveurs pour venir chercher la préparation.
    * il manque une préparation pour la commande, la commande est alors en attente de la préparation manquante.
      Et attend qu'un cuisinier cuisine la préparation manquante.

----------------------------------------------------------------
</p>
</details>

## Diagrammes de cas d'utilisation

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

Le serveur a la possibilité de proposer le menu au client. Il pourra notamment prendre la commande de celui-ci. Pour cela, il devra saisir le numéro de table ainsi qu'ajouter une ou plusieurs préparations à la commande.  
Lorsqu'une préparation est ajoutée dans une commande, les préparateurs sont directement notifiés. Les serveurs ont également la possibilité de servir une partie de la commande dès lors qu'ils ont été notifiés par les préparateurs.  
Il peut également suivre l'état d'avancement de la commande. Dès que celle-ci est finie, le serveur pourra générer l'addition puis indiquer si le réglement a bien été réalisé.

### Cuisine

![GitHub Logo](/images/UC-Cuisine.png)

Le préparateur a la possibilité d'indiquer sur l'application la prise en charge d'une préparation. 
Dès qu'il a fini, il doit indiquer l'accomplissement de cette dernière. 
Cela a comme conséquence de notifier tous les serveurs. 
Il a également la possibilité d'indiquer qu'une préparation est indisponible.

### Gérer le menu

![GitHub Logo](/images/UC-Menu.png)

Le patron a la possibilité de gérer le menu, c'est-à-dire d'ajouter, de modifier et de supprimer une préparation d'un menu.

## Diagramme de packages

![GitHub Logo](/images/diagramme_packages.PNG)

### Explication du diagramme de packages
Ce document a pour but d'éclaircir les choix qui ont été fait pour le diagramme de packages.

#### Division en trois packages
La logique de l'application "One Minute" peut se diviser en trois grands "domaines" : la logique relative au personnel du restaurant, la logique relative à la gestion des préparations que propose le restaurant et la logique relative à la gestion des commandes.

Pour respecter cette séparation de logique, il a été choisi de décomposer également les classes en trois grands paquetages : le **personnel**, la **carte** et les **commandes**.

#### Personnel
Ce package contient toutes les classes liées aux utilisateurs de l'application : les employés du restaurant. Ce package est dépendant des deux autres packages car le personnel manipule les données du système.

#### Carte
La carte est le package représentant les plats, desserts, préparations etc du restaurant. Ce package ne dépend d'aucun autre car il représente avant tout les classes qui seront manipulées par les autres packages.

#### Commandes
Le package des commandes représente toute la logique des commandes, de sa création en table à l'addition. Les commandes sont dépendantes de la carte ainsi que du personnel.

## Diagramme de classes

![GitHub Logo](/images/diagramme_classe.PNG)

### Explication du diagramme de classe
Ce document a pour but d'éclaircir ou de justifier certains choix dans le diagramme.

#### Les utilisateurs
- **MembrePersonnel** représente tout utilisateur connecté de l'application et contient les infos de ces utilisateurs.
- **Patron**, **Serveur** et **Préparateur** représentent les différents utilisateurs pouvant se connecter et héritent donc de **MembrePersonnel**
- **Préparateur** représente tout membre du restaurant faisant partie des cuisines
	- *Exemple : glacier, barman, cuisinier...*

#### Classe "Table"
- Les clients, qui ne manipulent pas directement l'application, s'installe à des **Tables** qui seront utilisées pour la gestion des commandes dans le système.
- Les clients n'ont donc pas de représentation dans le système puisqu'ils n'interagissent pas avec ce dernier.
- Chaque table possède un **numéro** unique.
- Lorsque le client commence sa commande, celle-ci devient la **commandeEnCours** de la table.
- Lorsque l'addition est réglée, la **commandeEnCours** s'ajoute aux **commandesPassées** de la table.
	- Le champ **commandesPassées** est *additionnel* et existe à des fins d'historique non nécessaires dans l'immédiat.

#### Gestion du menu
- Une **Préparation** représente un plat, une entrée, un dessert, etc
- Une **Préparation** peut être reliée à une **Catégorie**.
- **Catégorie** représente une catégorie de préparation telle que *Poisson, viande, dessert, boisson, etc*
- Le **prix** d'une **Préparation** représente le prix courant de cette préparation à la carte.
- Un **Menu** propose plusieurs **Préparations** et une **Préparation** peut être proposée par plusieurs **Menus** différents.
- Il n'existe qu'un seul **Menu** courant qui est celui sur lequel on peut commander durant le service.
- Un **Patron** a tous les droits sur tous les **Menus**, il peut donc les créer/modifier/supprimer/etc.
- Une **Préparation** peut être temporairement **indisponible** (on ne peut plus la commander).

#### Gestion de la commande
- Une **Commande** possède plusieurs **états** : 
	- *Créée*, *En cours*, *Annulée*, *Terminée*
- Afin d'éviter des calculs inutiles, la **Commande** retient son **prix total**
- Une **Commande** possède plusieurs **LigneCommande**.
- Une **LigneCommande** représente une **Préparation** choisie par le client ainsi que la quantité de cette **Préparation** à faire (ex : 2 spaghettis)
	- **Explication** : comme un client ne commande pas toujours tout ce qu'il veut en un coup au restaurant, il est plus sage de décomposer la commande en plusieurs lignes correspondant à ses demandes.
- Une **LigneCommande** possède elle-même plusieurs états :
	- *En attente*, *En cours*, *Terminée*, *Servie*, *Annulée*
- La **LigneCommande** est la donnée la plus manipulée par le système puisqu'elle sera :
	- créée par un serveur quand il **prend note** des demandes d'une table
	- notifiée en cuisine et *en attente* d'une prise en charge en cuisine.
	- *en cours* quand elle sera prise en charge en cuisine.
	- notifiée en service et *terminée* quand la prise en charge en cuisine est finie.
	- *servie* à la table par le serveur.
	- *annulée* si un problème survient.
- Une **LigneCommande** possède un **prix** (le prix total de la ligne s'obtient en faisant ``prix * quantité``)
	- **Explication** : on ne peut pas se référer au prix courant dans la classe **Préparation** car ce prix courant change au cours du temps. Cependant, si je veux consulter l'état d'une commande d'il y a un mois, peut-être que le prix de mes spaghettis ont changé. Ceci m'amènerait à voir un prix qui n'est pas celui qui était correct un mois auparavant.
- Un **Préparateur** qui prend en charge une **LigneCommande** va générer une **PriseEnCharge**.
	- **Explication** : si une **LigneCommande** demande 64 spaghettis, il est peu probable qu'un seul **Préparateur** s'en charge. Donc chaque **Préparateur** choisit la **quantité** de spaghettis dont il s'occupera.
- Une **PriseEnCharge** a trois **états** :
	- *En cours*, *Terminée*, *Annulée*

## Premières versions des maquettes

Ces maquettes seront amenées à changer, il s'agit de nos premières versions.

L'application aura plusieurs vues en fonction des utilisateurs. Chaque vue sera selectionnable à gauche de l'écran. Nous souhaitons laisser à tous les membres du restaurant la possibilité de voir les différentes parties de l'application. A priori, les accès seront donnés par des managers. Le mieux sera de le faire en début de chaque jour, avant le service.

Le but de l'application est de gagner du temps. Notre application ne doit donc pas alourdir la charge de travail des préparateurs. Nous ne connaissons pas le nombre de tablettes disponibles dans le restaurant, nous en comptons une par serveur pour le moment, et une ou deux en cuisine. Il sera tout à fait possible d'en mettre moins, car nous sommes bien conscients qu'une tablette coûte assez chère. Cela pose donc certains problèmes, en effet, les préparateurs ne doivent pas perdre de temps en se connectant. C'est pourquoi, nous vous proposons d'utiliser notre application avec un compte pour la cuisine. Chaque préparateur doit juste s'identifier en cliquant sur un bouton avec son nom pour que l'on sache qui cuisine quoi. Cela leur permet de ne pas avoir à rentrer leur mot de passe. 

### Maquette de la partie cuisine

#### Première version 

Dans cette version pour pouvons observer qu'il y aura deux vues pour les préparateurs. Une première vue avec les catégories de plats, et une seconde en fonction des commandes. Le but des catégories était de faire gagner du temps aux préparateurs. Etant donné le fait que la vue des commandes est aussi importante, nous allons aussi la laisser.

![GitHub Logo](/Maquettes/1.0.0/Cuisine.png)

Suite à la création de cette maquette nous ai venu l'idée de laisser la possibilité aux préparateurs de ne pas perdre de temps en s'identifiant. C'est pourquoi ils auront juste à appuyer sur leur photo à droite, valider leur nom et choisir le plat qu'ils veulent s'approprier ou valider.

![GitHub Logo](/Maquettes/2.0.0/Cuisine.png)

### Maquette de la partie service

Dans cette version, l'idée était de permettre aux serveurs de recréer le restaurant sous la forme d'une vue. Ceci avait pour but de savoir quelle table était laquelle. Malheureusement cette solution étaient assez technique et allait prendre du temps.

![GitHub Logo](/Maquettes/1.0.0/Service.png)

La seconde solution était plus portée sur quelque chose de plus simple techniquement. Mais, cela a permit de voir l'avancement des commandes plus facilement.

![GitHub Logo](/Maquettes/2.0.0/Service.png)


## Glossaire métier

- ***Addition*** : facture de la commande indiquant la liste des préparations commandées ainsi que le montant total de la commande
- ***Commande*** : Note qui sert à savoir ce que le client a choisi. Elle est prise par un serveur, et est transmise aux cuisines.
- ***État*** : état d'avancement de la commande.
- ***Indisponible*** : Etat d'une préparation qui ne peut pas/plus être réalisée par manque de un (ou plusieurs) ingrédient(s) la constituant.
- ***Partie de la commande*** : pack de boissons, de plats ou de desserts etc.
- ***Réapprovisionnement*** : Action de recevoir un nouvel apport de marchandises afin de renouveler les stocks.
- ***Stock*** : Ingrédients disponibles pour préparer les commandes.

## Méthode de travail
Ce document sert à expliquer la manière générale dont on travaille.

### En séance
L'objectif de nos deux heures de TPs par semaine est principalement de débattre de nos manières de voir la solution au problème posé. Nous ne nous concentrons donc pas directement sur l'élaboration du travail mais préférons prendre le temps d'entrechoquer nos idées pour produire un travail étant le fruit de nos meilleures réflexions.

Nous pensons que, en faisant cela, nous gagnons au final du temps à ne pas repasser plusieurs fois sur notre travail.

### En dehors des séances
- Pour organiser le travail à faire pour chaque semaine, il a été décidé d'utiliser **Trello**.

- Le dépôt Git de l'école étant encore indisponible pour la majorité des alternants suite à des retards administratifs, un deuxième ``remote`` sur **Github** a été installé temporairement à [cette adresse](https://github.com/canoenZoe/One_Minute.git).

- Pour faciliter les discussions moins formelles entre nous, nous utilisons un réseau de chat en ligne (Facebook Messenger).

- La complétion du document de suivi pour le groupe (document Excel) est réalisée avec Google Drive, qui offre un système de modifications collaboratives.

- Google Drive est utilisé pour partager les diverses ressources annexes.

## Retroplanning


### Retroplanning de BARCHID Sami

#### Tâches faites

- Élaboration des diagrammes de classe
- Élaboration du diagramme de package
- Élaboration de scénarios concrets

#### Méthode de travail

Ma manière de travailler personnelle dans le projet a été de profiter des TPs pour mixer un maximum des jugements de chacun sur tous les travaux à réaliser (diagrammes, scénarios, etc) afin d'être directement fixé sur la façon de remplir mes tâches. Personnellement, je pense que les deux heures de TPs par semaine sont plus utiles si on les utilise pour entrechoquer nos idées que réellement écrire quelque chose qui ne satisfait pas tout le monde.

#### Difficultés

La principale difficulté vue pour ce projet est l'absence totale de client à qui poser des questions, laissant les ambiguïtés de "l'appel d'offre" à notre appréhension personnelle.

Une difficulté, plus secondaire, est la différence de compréhension des standards UML entre tous (élèves, professeurs et manuels compris), qui souligne bien l'importance d'établir des conventions entre les différents membres de l'équipe. Cette difficulté est surmontée grâce aux différents débats entre nous lorsqu'une ambiguïté était rencontrée.

### Retroplanning de Laurine Drodzinski

#### Travail effectué

Au cours de cette première itération j'ai eu l'occasion de travailler sur les scénarios. Après en avoir réalisé, j'ai pu retravailler le reste des scénarios afin qu'ils soient cohérents tant au niveau des acteurs, de la présentation, du vocabulaire etc.  
J'ai également travaillé sur le tableau regroupant divers termes utilisés au cours de cette itération.
Ensuite, j'ai décrit les différents acteurs de l'application en indiquant leurs possibilités d'actions ainsi que quelques contraintes les concernant.
Par ailleurs, j'ai pu accompagner Anthony sur les diagrammes de cas d'utilisation.
Puis, pour finir, j'ai corrigé les fautes d'orthographes des différents fichiers du git ainsi que remis en forme divers tableaux et dossiers.

#### Difficultés rencontrées

J'ai rencontré quelques problèmes de compréhension au début de projet concernant l'organisation du projet.
En effet nous avions éparpillé des données sur diverses plateformes. Cependant ce problème fut très rapidement réglé car dès la deuxième séance nous nous sommes réorganisés et nous avons regroupés les informations sur git.

Le second soucis a été une confusion à propos de certaines informations du cours. Notamment au niveau des diagrammes de cas d'utilisation  et des différentes flèches à utiliser. Afin de régler ce problème nous nous sommes rapprochés de Cédric Dumoulin qui nous a réexpliqué leur sens.


### Retroplanning de Zoé Canoen

#### Tâches faites

- Mise en place des différents outils lors du début du projet
- Gestion de la répartition des charges au sein de l'équipe
- Synthèse des séances
- Rendu du lot 1 (format markdown et pdf)
- Premières maquettes de l'application (format fixe)

#### Méthode de travail

Pour moi il est important d'avoir une vision globale du sujet. Cela permet de gérer au mieux les délais. La répartition des tâches et la confiance en chacun des membres de l'équipe est primordiale. J'aime apporter des nouvelles idées et je pense que la communication dans l'équipe est importante. Au début je parlais à chacun, mais maintenant nous faisons des réunions tous ensemble, et je trouve que c'est une bonne idée pour tout mettre en commun.

#### Difficultés

Je pense que nous avançons très bien, et que nous faisons face à tous les évenements sans trop de difficultés. La capacité d'adaptation du groupe est très importante. Je suis bien consciente que ce n'est pas le seul projet sur lequel nous devons travailler, et que parfois certaines personnes dans le groupe n'ont pas le temps de travailler GL. Mais notre groupe se rééquilibre toujours pour continuer à avancer. Si une personne travaille beaucoup plus que les autres, je veille à ce que ces tâches soient minimiser. Et à l'inverse, si une  personne n'a pas le temps de réaliser une tâche, je m'arrange pour que la tâche soit redistribuée si les délais sont trop courts. Nous nous faisons confiance sur le travail effectué, chaque personne travaille dans la mesure de son temps disponible, et fini toujours par rattraper son retard quand elle le peut. Nous pouvons tous compter sur les autres si besoin, et donc avancer à notre rythme.

#### Ressenti

J'aurai adoré n'avoir que GL à travailler ce semestre. C'est rééllement une matière fort intéréssante. Au début nous devions trouver notre rythme de croisière et je crois que nous l'avons trouvé. Les réunions de groupe lors des tps sont vraiment très utiles et nous avançons beaucoup. Chacun peut ainsi avoir une vision globale du projet.

### Retroplanning de Anthony SLIIMANI

#### Tâches faites

- Élaboration de scénarios concrets & un alternatif
- Élaboration des diagrammes des cas d'utilisations
- Participation à l'élaboration du diagramme de classess


#### Difficultés
On a pu constater un début difficile au niveau de l'organisation mais nous avons pu nous harmoniser au fil des semaines. Nous avons des idées intéressantes mais parfois qui s'écarte un peu trop du sujet principal ou encore n'a pas la nécessité d'être élaborer pour cette première itération. Nous avons eu quelques difficulés sur les standarts UML en contatant diverses divergences avec le cours, les livres de référence ou encore des documents sur Internet.

#### Ressenti

Cette itération m'a montré que toute l'équipe était motivé pour ce début de projet. J'espère que cette motivation va perdurer durant les prochaines itérations. Une bonne cohésion d'équipe s'est formé durant ces quelques semaines. Tout le monde essaye de s'adapter aux autres, à son rythme. J'aime beaucoup la manière que chacun appréhende le sujet, de voir la diversité de nos idées et l'ouverture d'esprit de chacun lors des échanges de nos idées pour parvenir à une solution qui correspond le plus aux besoins du client.

### Retroplanning of Noura

#### Done tasks
Description of case of use 
Package diagram elaboration of one version
contribution in the glossary elaboration

#### Work's Method
For me, working within  a team is a greatfull experience ; during the "TP" , I try usually to understand the ideas of my colleagues 
and mainly try to explain mine.
The most important thing that I try to get it after each meeting is to gather what Mr Michaël Launay tells us and what we sugggess to do as a srategy. Even between us, we have really many points of view, so that to make a collective decision is really so interesting.

#### Difficulties
If I will speak about difficulties, I will start by the différence of language with our responsible and with my colleagues. After each meetiig, and whan I come back to home i try to remember the most important suggession, sentences and even words and I start "traduction service", it takes much time. Besides, one of the most things that was difficult for me, is that our project seems to be clear in his glabal view : "take an order inside a restaurant", but  some details about at which level we are limited to designing this application ; should we just take into consideration "the service  give by the waiter" or may be be so selective when we had to choose the performance evaluation criterion (good service/client satisfaction/price/time taken by the application), make it a bit complicated.



