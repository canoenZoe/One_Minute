# Retirer une préparation au menu

### Nom
Retirer une préparation au menu.

### Résumé
Le patron retire une préparation à un menu qu'il a choisit.

### Acteurs
- Patron

### Déclenchement
Le patron indique qu'il veut retirer une préparation au menu.

### Pré-condition
- Le patron est authentifié dans le système.
- Le patron a choisi le menu sur lequel il veut retirer une préparation.

### Post-condition
- La préparation choisie est retirée du menu.

### Scénario nominal
1. Le patron indique qu'il veut retirer une préparation au menu.
2. Le système affiche les préparations du menu.
3. Le patron choisit la préparation à retirer.
4. Le système valide la préparation choisie.
5. Le système supprime la préparation du menu.
6. Le système enregistre la suppression par le patron.
7. Fin du CU.

### Scénarios alternatifs
- 4.a. [La préparation choisie n'est pas valide / est déjà retirée]
	- 4.a.1. Le système affiche un message d'erreur.
	- 4.a.2. Retour à l'étape 2.

### Scénarios d'exception
- 2.b. [Aucune préparation n'existe dans le menu]
	- 2.b.1. Le système affiche un message d'erreur.
	- 2.b.2. Le système revient à son état d'avant le déclenchement.
	- 2.b.3. Fin du CU.
- *.a. [Panne de réseau]
	- *.a.1 Le système indique que le réseau a été coupé.
	- *.a.2 Le système retourne à son état d'avant le déclenchement.
	- *.a.3 Fin du CU.

### Informations supplémentaires
- **Version** : 1
- **Date de création :** 14/10/2018
- **Responsable** : BARCHID Sami