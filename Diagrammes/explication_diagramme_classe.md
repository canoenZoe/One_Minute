# Explication du diagramme de classe
Ce document a pour but d'éclaircir ou de justifier certains choix dans le diagramme.

## Les utilisateurs
- **MembrePersonnel** représente tout utilisateur connecté de l'application et contient les infos de ces utilisateurs.
- **Patron**, **Serveur** et **Préparateur** représentent les différents utilisateurs pouvant se connecter et héritent donc de **MembrePersonnel**
- **Préparateur** représente tout membre du restaurant faisant partie des cuisines
	- *Exemple : glacier, barman, cuisinier...*

## Classe "Table"
- Les clients, qui ne manipulent pas directement l'application, s'installe à des **Table** qui seront utilisées pour la gestion des commandes dans le système.
- Les clients n'ont donc pas de représentation dans le système puisqu'ils n'interagissent pas avec ce dernier.
- Chaque table possède un **numéro** unique.
- Lorsque le client commence sa commande, celle-ci devient la **commandeEnCours** de la table.
- Lorsque l'addition est réglée, la **commandeEnCours** s'ajoute aux **commandesPassées** de la table.
	- Le champ **commandesPassées** est *additionnel* et existe à des fins d'historique non nécessaires dans l'immédiat.

## Gestion du menu
- Une **Préparation** représente un plat, une entrée, un dessert, etc
- Une **Préparation** peut être reliée à une **Catégorie**.
- **Catégorie** représente une catégorie de préparation telle que *Poisson, viande, dessert, boisson, etc*
- Le **prix** d'une **Préparation** représente le prix courant de cette préparation à la carte.
- Un **Menu** propose plusieurs **Préparations** et une **Préparation** peut être proposée par plusieurs **Menus** différents.
- Il n'existe qu'un seul **Menu** courant qui est celui sur lequel on peut commander durant le service.
- Un **Patron** a tous les droits sur tous les **Menus**, il peut donc les créer/modifier/supprimer/etc.
- Une **Préparation** peut être temporairement **indisponible** (on ne peut plus la commander).

## Gestion de la commande
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
	- *annulée* si un problème surviendrait.
- Une **LigneCommande** possède un **prix** (le prix total de la ligne s'obtient en faisant ``prix * quantité``)
	- **Explication** : on ne peut pas se référer au prix courant dans la classe **Préparation** car ce prix courant change au cours du temps. Cependant, si je veux consulter l'état d'une commande d'il y a un mois, peut-être que le prix de mes spaghettis ont changé. Ceci m'amènerait à voir un prix qui n'est pas celui qui était correct un mois auparavant.
- Un **Préparateur** qui prend en charge une **LigneCommande** va générer une **PriseEnCharge**.
	- **Explication** : si une **LigneCommande** demande 64 spaghettis, il est peu probable qu'un seul **Préparateur** s'en charge. Donc chaque **Préparateur** choisit la **quantité** de spaghettis dont il s'occupera.
- Une **PriseEnCharge** a trois **états** :
	- *En cours*, *Terminée*, *Annulée*