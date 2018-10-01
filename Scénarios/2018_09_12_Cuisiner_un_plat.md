# Cuisiner un plat

---

### Description :

***Roger*** désire faire un plat, et doit informer l'application sur quel(s) plat(s) il est en train de cuisiner.

---

### Scénario :

- ***Roger*** veut cuisiner un (ou plusieurs) plat(s).
- ***Roger*** choisi un (ou plusieurs) plat(s) qu'il s'apprete à cuisiner. 
- ***Roger*** valide et peut commencer à cuisiner.
- Une fois que ***Roger*** a terminé son plat, il s'identifie à nouveau pour dire qu'il a terminé un plat.
- Ensuite, SOIT 
    * son plat permet de terminer une ***partie de la commande***, 
      dans ce cas une notification est envoyée aux serveurs pour venir chercher le plat.
    * il manque un plat pour la commande, la commande est alors en attente du plat manquant. 
      Et attend qu'un cuisinier cuisine le plat manquant.

---

### Glossaire :

- ***Roger*** : cuisinier
- ***partie de la commande*** : pack de boissons, de plats ou de desserts etc.
