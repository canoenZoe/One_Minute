# Imprimer l'addition d'une commande  

------

**Nom du cas :** Imprimer l'addition d'une commande
**But :** Le client souhaite avoir le détails de sa commande / justificatif de paiement de sa commande sous forme physique.
**Acteur principal :** Serveur
**Date de création : **19/10/2018
**Nom du responsable de création :** Anthony SLIMANI
**Dernière date de mise à jour : ** 06/11/2018
**Nom du responsable de la dernière modification : **Anthony SLIMANI
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**  

- L'état de réglementation de la commande est à *"Réglé"*
- Le serveur consulte la commande qui doit être imprimer sur le ***support technique***

**Déclenchement :** 

- Le client demande au serveur l'impression du détails de sa commande / justificatif de paiement

**Scénario nominal :**  

1. Début du scénario
2. Le serveur indique au système que le détails d'une commande doit être imprimé
3. Le système envoie le détails de la commande à l'appareil d'impression
4. L'appareil d'impression effectue l'impression
5. L'appareil d'impression au système quand l'impression est terminé
6. Le système affiche au serveur que l'impression est terminé
7. Le serveur apporte l'impression du détails de la commande au client
8. Fin du scénario

**Post-condition :**

- Le client a reçu son détails de commande / justificatif de paiement de sa commande sous forme physique.

**Scénarios alternatifs :**  

- [***L'appareil d'impression n'a pas la possibilité d'imprimer***]
  - Le système affiche un message d'erreur avec un message indiquant la cause
  - Le serveur indique qu'il souhaite

**Scénario d'exception :**  

- [La communication entre l'appareil d'impression et le système n'est pas possible]
  - Le système affiche un message d'erreur au serveur
  - Le serveur peut réintérer l'établissement de la communication entre l'appareil et l'appareil d'impression

------

### Glossaire :

- ***L'appareil d'impression n'a pas la possibilité d'imprimer*** : coupure de la communication entre l'appareil d'impression et le système, plus d'encre, plus de papier

