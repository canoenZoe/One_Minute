# Imprimer l'addition d'une commande  

------

**Nom du cas :** Imprimer l'addition d'une commande
**But :** Le client souhaite avoir le détails de sa commande / justificatif de paiement de sa commande sous forme physique.
**Acteur principal :** Serveur
**Date de création : **19/10/2018
**Nom du responsable de création :** Anthony SLIMANI
**Dernière date de mise à jour : ** 30/10/2018
**Nom du responsable de la dernière modification : **Anthony SLIMANI
**Version :** 1

------

*Ce scénario prend en compte les conditions explicitées dans le document "Général.md".*

------

**Pré-conditions :**  

- La commande est à l'état 'Réglé'
- Le serveur est toujours sur la commande qui doit être imprimer sur la tablette

**Déclenchement :** 

- Le client demande un justificatif au serveur

**Scénario nominal :**  

1. Début du scénario
2. Le client demande au serveur l'impression du détails de sa commande / justificatif de paiement
3. Le serveur indique au système que le détails d'une commande doit être imprimé
4. Le système vérifie si la communication entre celui-ci et l'appareil d'impression est possible
5. Le système envoie le détails de la commande à l'appareil d'impression
6. L'appareil d'impression effectue l'impression
7. Le système indique au serveur quand l'impression est terminé
8. Le serveur apporte l'impression du détails de la commande au client
9. Fin du scénario

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

