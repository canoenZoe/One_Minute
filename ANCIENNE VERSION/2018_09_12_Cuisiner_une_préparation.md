# Cuisiner une préparation

---

### Description :

***Roger*** désire faire une préparation, et doit informer l'application sur quelle(s) préparation(s) il est en train de cuisiner.

---

### Scénario :

- ***Roger*** veut cuisiner une (ou plusieurs) préparation(s).
- ***Roger*** choisi une (ou plusieurs) préparation(s) qu'il s'apprête à cuisiner. 
- ***Roger*** valide et peut commencer à cuisiner.
- Une fois que ***Roger*** a terminé sa préparation, il s'identifie à nouveau pour dire qu'il a terminé une préparation.
- Ensuite, SOIT 
    * sa préparation permet de terminer une ***partie de la commande***, 
      dans ce cas une notification est envoyée aux serveurs pour venir chercher la préparation.
    * il manque une préparation pour la commande, la commande est alors en attente de la préparation manquante. 
      Et attend qu'un cuisinier cuisine la préparation manquante.

---

### Glossaire :

- ***Roger*** : cuisinier
- ***partie de la commande*** : pack de boissons, de plats ou de desserts etc.
