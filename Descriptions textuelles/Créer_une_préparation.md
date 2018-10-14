# Créer une préparation

### Nom
Créer une préparation.

### Résumé
Le patron ajoute une préparation.

### Acteurs
- Patron

### Déclenchement
Le patron indique qu'il veut créer une préparation.

### Pré-condition
- Le patron est authentifié dans le système.

### Post-condition
- La nouvelle préparation est créée dans le système.
- La nouvelle préparation peut être créée dans des menus.

### Scénario nominal
1. Le patron indique qu'il veut créer une préparation.
2. Le système demande au patron d'entrer les données de la préparation.
3. Le patron entre les données de la préparation.
4. Le système valide les données de la préparation.
5. Le système enregistre la nouvelle préparation.
6. Le système indique au patron que la préparation est créée.
7. Fin du CU.

### Scénarios alternatifs
- 4.a. [Les données ne sont pas valides / La préparation entrée existe déjà]
	- 4.a.1. Le système affiche un message d'erreur.
	- 4.a.2. Retour à l'étape 2.

### Scénarios d'exception
- *.a. [Panne de réseau]
	- *.a.1 Le système indique que le réseau a été coupé.
	- *.a.2 Le système retourne à son état d'avant le déclenchement.
	- *.a.3 Fin du CU.

### Informations supplémentaires
- **Version** : 1
- **Date de création :** 14/10/2018
- **Responsable** : BARCHID Sami