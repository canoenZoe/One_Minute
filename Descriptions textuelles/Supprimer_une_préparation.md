# Supprimer une préparation

### Nom
Supprimer une préparation.

### Résumé
Le patron supprime une préparation existante.

### Acteurs
- Patron

### Déclenchement
Le patron indique qu'il veut supprimer une préparation.

### Pré-condition
- Le patron est authentifié dans le système.

### Post-condition
- La préparation est retirée du système

### Scénario nominal
1. Le patron indique qu'il veut supprimer une préparation.
2. Le système affiche les préparations existantes.
3. Le patron choisit la préparation à supprimer.
4. Le système demande la confirmation du choix.
5. Le patron confirme le choix de la préparation à supprimer.
6. Le système valide la préparation à supprimer.
7. Le système supprime la préparation.
8. Le système indique au patron que la préparation est supprimée.
9. Fin du CU.

### Scénarios alternatifs
- 5.a. [Le patron infirme la suppression de la préparation choisie]
	- 5.a.1. Le système affiche un message d'erreur.
	- 5.a.2. Retour à l'étape 2.
- 6.a. [La préparation choisie n'est pas valide/est déjà supprimée]
	- 6.a.1. Le système affiche un message d'erreur.
	- 6.a.2. Retour à l'étape 2.
- 6.b. [La préparation choisie est utilisée dans un/des menu(s)]
	- 6.b.1. Le système indique au patron que la préparation est utilisée dans un/des menu(s).
	- 6.b.2. Le système affiche les menus où la préparation est utilisée.
	- 6.b.3. Le patron confirme la suppression de la préparation.
	- 6.b.4. Aller à l'étape 7.

### Scénarios d'exception
- 6.b.3.a. [Le patron refuse la suppression de la préparation]
	- 6.b.3.a.1. Le système annule la suppression de la préparation.
	- 6.b.3.a.2. Le système retourne à son état d'avant le déclenchement.
	- 6.b.3.a.3. Fin du CU.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.

### Informations supplémentaires
- **Version** : 1
- **Date de création :** 14/10/2018
- **Responsable** : BARCHID Sami
