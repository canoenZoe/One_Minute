# Architecture de l'application

![GitHub Logo](/Architecture/image.png)

L'application sera construite sur un modèle en 3 couches. La couche la plus importante sera la couche métier. C'est celle qui répondra au besoin métier du client.
Nous ajouterons à cette couche une base de donnée pour stocker nos données, nous utiliserons un DAO pour avoir accès à la base de donnée.
Pour finir, pour l'aspect visuel nous utiliserons le modèle MVC qui nous permettra de faire le lien avec notre modèle métier. Nous aurons donc deux modèles, un modèle métier et un modèle pour la vue. 
