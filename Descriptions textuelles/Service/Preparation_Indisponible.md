# Préparation indisponible

---

**Nom du cas :** Préparation indisponible  
**But :**  
**Acteur principal :** Serveur  
**Date de création :** 06/11/2018  
**Nom du responsable de création :** Zoé Canoen  
**Dernière date de mise à jour :** 06/11/2018  
**Nom du responsable de la dernière modification :** Zoé Canoen  
**Version :** 1

---

*Ce scénario prend en compte les conditions et le glossaire explicités dans le document "Général.md".*

Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".

------

**Pré-conditions :**  

- Le client a passé une commmande.

**Déclenchement :**

- Une préparation de la commande du client n'est plus disponible
- La préparation a été indiqué comme indisponible par la cuisine

**Scénario nominal :**  

1. Le système change l'état de la ligne de commande en "annulée" sur les lignes de commandes contenant des préparations indisponibles.
2. Le serveur va à la table où le plat est indisponible.
3. Le client peut choisir à ce moment un nouveau plat disponible.

**Scénarios alternatifs :**  

- La préparation est de nouveau disponible car il y a eu un réaprovisionnement, dans ce cas, on ne fait rien.

**Scénario d'exception :**  

- Néant

------

**Diagramme de séquence :**

![GitHub Logo](/Diagrammes_Sequences/DS-Preparation_Indisponible(service).png)
