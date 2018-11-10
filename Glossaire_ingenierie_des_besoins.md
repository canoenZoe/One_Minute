
# Glossaire de l'ingénierie des besoins

## Portée
Ce glossaire présente et détaille les termes et concepts liés au vocabulaire technique de la solution développée.

## Avertissement
Il est supposé ici que le lecteur possède déjà des connaissances techniques de base dans les domaines de l'orientée objet et des diagrammes UML.

## Organisation
Le glossaire s'organise en une suite de définitions des différents termes, divisée en sous-catégories relatives aux différentes phases d'analyse.

Chaque terme est décrit en trois parties : un énoncé du terme, sa définition et sa traduction anglaise.

## Définitions

### Modèle fonctionnel
|  Terme| Définition | Traduction |
|--|--|--|
|Exigences fonctionnelles|Exigences à prendre en compte lors de la création du système et qui est liées aux besoins fonctionnels du client.|Functional requirements|
Exigences non-fonctionnelles|Exigences à prendre en compte lors de la création du système et qui n'est pas liées aux besoins fonctionnels du client.|Nonfunctional requirements|
|Scénario concret|Scénario sus forme libre (texte, vidéo, bande dessinée,...) qui sert à décrire, à travers un récit, une manière d'utiliser le système à développer. Un scénario concret est abstrait de toutes les notions techniques du système.|Scenario|

### Modèle objet (architecture)
|  Terme| Définition | Traduction |
|--|--|--|
|Objet frontière|Objet du système dont le rôle est de gérer l'interaction avec l'utilisateur (affichage, etc).|Boundary object|
|Objet de contrôle|Objet du système dont le rôle est de gérer la logique métier du système.|Control Object|
|Objet entité|Objet du système chargé de représenter les données persistées dans la base de données.|Entity object|
|Objet d'accès aux données|Objet du système dont le rôle est de gérer la logique de gestion des données.|Data Access Object (DAO)|
|Objet d'interface utilisateur|Objet du système dont le rôle est de représenter les interfaces affichées à l'utilisateur.|User Interface Object (UI)|

### Modèle dynamique
|  Terme| Définition | Traduction |
|--|--|--|
|Diagramme de séquence système (DSS)|Diagramme de séquence dont le rôle est de représenter les interactions entre les acteurs et le système. Ce dernier est vu sous forme de boîte noire (pas de spécification de son modèle objet).|System Sequence Diagram|
|Description textuelle/Scénario abstrait|Reprise de chaque cas d'utilisation sous forme textuelle pour décrire une interaction entre le système et l'acteur.||
