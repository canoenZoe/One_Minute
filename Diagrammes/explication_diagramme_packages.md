
# Diagramme de packages

## Organisation
L'application est composée de 5 principaux packages :

- **boundaries** : contient les classes Boundary du système. Ces classes s'occupent de gérer l'interaction avec l'utilisateur.
- **uis** : contient les classes UI du système. Ces classes s'occupent de l'aspect visuel du système.
- **controls** :  contient les classes Control du système. Ces classes implémentent la logique métier.
- **daos** : contient les classes DAO (Data Access Object). Ces classes s'occupent d'accéder et de gérer les données persistées dans la base de données.
- **entities** : contient les classes Entity du système. Ces classes sont des classes représentant les données persistées dans la base de données.

On distingue trois grandes logiques à laquelle répondent les packages :

### Interaction avec l'utilisateur
Représente toute la logique d'interaction avec l'utilisateur (affichage, etc).
Les packages **uis** et **boundaries** sont chargés d'assurer l'interaction avec l'utilisateur.
- **uis** : gère l'affichage.
- **boundaries** : gère les actions que peut effectuer un utilisateur sur le système.

### Logique métier (business)
Représente toute la logique métier derrière les cas d'utilisation.
Cette logique est implémentée par le package **controls**.

### Logique de gestion des données
Représente tout ce qui est lié à la gestion des données persistées en base de données par le système.
Cette logique est implémentée par les package **daos** et **entities**.

- **entities** : renferme les classes qui contiennent les données brutes en base de données. En bref, ce package renferme la représentation orientée objet des données persistées.
- **daos** : permet au système d'interagir avec la base de données.

## Les sous-packages
Les classes ne sont pas directement placées dans les packages principaux et sont divisées en plusieurs sous-packages, afin d'augmenter la granularité.

### boundaries, uis et controls
En ce qui concerne les packages **boundaries**, **uis** et **controls**, les classes sont divisées en sous-packages représentées par les trois contextes fonctionnels que nous avons définis dans nos diagrammes de cas d'utilisation :

- **carte** : gestion de la carte des menus/préparations/...
- **cuisine** : gestion de la logique pour les préparateurs (cuisiniers, barmar, etc)
- **service** : gestion de la logique pour les serveurs.

Ainsi, les classes de **uis.service** s'occupent de l'affichage pour les UC liés au contexte du service.

### entities et daos
Décomposer les entités et daos suivant les contextes fonctionnels des UC n'étaient pas une bonne idée pour les entités et daos puisque ces packages s'occupent essentiellement de la **logique de gestion de données**.

Trois types de sous-packages sont définis :
- **personnel** : gestion des données des préparateurs/serveurs/etc
- **commandes** : gestion des données des commandes
- **carte** : gestion des données de la carte.

## Dépendances entre packages
- Les objets **boundaries** *créent et renvoient* les objets **uis**.
- Les objets **boundaries** *appellent* la logique métier implémentée dans les objets de **controls**.
- Les objets de **controls** *appellent* la gestion de données des objets **daos**.
- Les objets **daos**, après avoir interagit avec la base de données, *manipulent* les objets **entities**.
- Les objets **controls** récupèrent les objets **entities** pour appliquer la logique métier sur ceux-ci.



## Patterns impliqués

### Les singletons
Les objets **controls**, **daos** et **boundaries** sont des **objets de service**. C'est-à-dire que ce sont des objets immuables (n'ont pas un état qui peut être modifié) et qu'ils sont utilisés pour les services qu'ils offrent (méthodes).

Ils doivent, cependant, être disponibles à tout moment de l'application. Il est, de plus, inutile qu'il y ait plusieurs objets de service pour une application. C'est pourquoi il a été choisi d'implémenter le pattern **Singleton**.

Il a été choisi de faire une implémentation différente du pattern Singleton, en passant par l'**injection de dépendance**. 
En effet, la manière classique d'implémenter un Singleton est contraignante, rajoute une logique de garantie du Singleton qui complexifie le code et crée une utilisation pervertie en cas d'abus. (Pour plus de précision, voir [cet article](https://dzone.com/articles/singleton-anti-pattern)).

### Pattern Observer
La cuisine doit être notifié d'une prise de commande tandis que le service doit être notifié lorsque la cuisine a terminé de préparer une commande. Ces deux cas d'utilisation requièrent la mise en place d'un service de notification.

Pour que ce service de notification fonctionne, il faut implémenter le **pattern Observer**. Les objets de controls de la prise d'une commande et de prise en charge d'une commande deviennent les **Subjets** du pattern, tandis que le service de notificiation est l'**Observer** qui s'abonne aux sujets.