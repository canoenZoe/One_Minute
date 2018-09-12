# Cuisiner un plat

### Description :

Un cuisinier désire faire un plat, et doit informer l'application sur quel(s) plat(s) il est en train de cuisiner.

### Scénario :

- Miguel veut cuisiner un (ou plusieurs) plat(s).
- Il valide son identité pour voir les plats qui lui sont assignés.
- Il choisi un (ou plusieurs) plat(s) qu'il s'apprete à cuisinier. 
- Il valide et peut commencer à cuisiner.
- Une fois qu'il a terminé son plat, il s'identifie à nouveau pour dire qu'il a terminé un plat.
- Ensuite, SOIT 
    * son plat permet de terminer une partie de la commande (par exemple toutes les entrées), 
      dans ce cas une notification est envoyée aux serveurs pour venir chercher le plat.
    * il manque un plat pour la commande, la commande est alors en attente du plat manquant. 
      Et attend qu'un cuisinier cuisine le plat manquant.
