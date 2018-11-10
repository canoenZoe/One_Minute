# Imprimer l'addition d'une commande  

------

**Nom du cas :** Imprimer l'addition d'une commande  
**But :** Le client souhaite avoir le détails de sa commande sous forme physique  
**Acteur principal :** Serveur  
**Date de création :** 19/10/2018  
**Nom du responsable de création :** Anthony SLIMANI  
**Dernière date de mise à jour :** 06/11/2018  
**Nom du responsable de la dernière modification :** Anthony SLIMANI  
**Version :** 2.2

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

Ce scénario prend en compte le glossaire explicité dans le document "Glossaire.md".

------

**Pré-conditions :**  

- Le serveur consulte la commande qui doit être imprimée sur le ***support technique***
- L'état de réglementation de la commande est à *"Réglé"*

**Déclenchement :**

- Le client demande au serveur l'impression du détail de sa commande

**Scénario nominal :**  

1. Début du scénario
2. Le serveur indique au système que le détail d'une commande doit être imprimé
3. Le système envoie le détail de la commande à l'appareil d'impression
4. L'appareil d'impression effectue l'impression
5. Le système affiche au serveur que l'impression est terminée
6. Le serveur apporte l'impression du détail de la commande au client
7. Fin du scénario

**Post-condition :**

- Le client a reçu le détail de sa commande sous forme physique.

**Scénarios alternatifs :**  

- Néant

**Scénario d'exception :**  

- 3.a [ ***L'appareil d'impression n'a pas la possibilité d'imprimer*** ]
  - 3.a.1 Le système affiche un message d'erreur avec un message indiquant la cause
  - 3.a.2 Fin du scénario

------

**Diagramme de séquence :**
