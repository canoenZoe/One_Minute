# Explication du diagramme de packages
Ce document a pour but d'éclaircir les choix qui ont été fait pour le diagramme de packages.

## Division en trois packages
La logique de l'application "One Minute" peut se diviser en trois grands "domaines" : la logique relative au personnel du restaurant, la logique relative à la gestion des préparations que propose le restaurant et la logique relative à la gestion des commandes.

Pour respecter cette séparation de logique, il a été choisi de décomposer également les classes en trois grands paquetages : le **personnel**, la **carte** et les **commandes**.

### personnel
Ce package contient toutes les classes liées aux utilisateurs de l'application : les employés du restaurant. Ce package est dépendant des deux autres packages car le personnel manipule les données du système.

### carte
La carte est le package représentant les plats, desserts, préparations etc du restaurant. Ce package n'est dépend d'aucun autre car il représente avant tout les classes qui seront manipulées par les autres packages.

### commandes
Le package des commandes représente toute la logique des commandes, de sa création en table à l'addition. Les commandes sont dépendantes de la carte ainsi que du personnel.