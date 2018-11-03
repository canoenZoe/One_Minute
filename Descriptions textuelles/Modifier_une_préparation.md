# Modifier une préparation

### Nom
Modifier une préparation.

### Résumé
Le patron modifie une préparation existante.

### Acteurs
- Patron

### Déclenchement
Le patron indique qu'il veut modifier une préparation.

### Pré-condition
- Le patron est authentifié dans le système.

### Post-condition
- La préparation est modifiée.

### Scénario nominal
1. Le patron indique qu'il veut modifier une préparation.
2. Le système affiche les préparations existantes.
3. Le patron choisit la préparation à modifier.
4. Le système valide la préparation à modifier.
5. Le système demande au patron d'entrer les modifications.
6. Le patron entre les données de modification de la préparation.
7. Le système valide la préparation modifiée.
8. Le système modifie la préparation.
9. Le système indique au patron que la préparation est modifiée.
10. Fin du CU.

### Scénarios alternatifs
- 4.a. [La préparation choisie n'est pas valide/n'existe pas]
	- 4.a.1. Le système affiche un message d'erreur.
	- 4.a.2. Retour à l'étape 2.
- 7.a. [Données invalides]
	- 7.a.1. Le système affiche un message d'erreur.
	- 7.a.2. Retour à l'étape 5.

### Scénarios d'exception
- 2.a. [Il n'y a aucune préparation existante]
	- 2.a.1. Le système affiche un message d'erreur.
	- 2.a.2. Le système revient à son état d'avant le déclenchement.
	- 2.a.3. Fin du CU.
- \*.a. [Panne de réseau]
	- \*.a.1 Le système indique que le réseau a été coupé.
	- \*.a.2 Le système retourne à son état d'avant le déclenchement.
	- \*.a.3 Fin du CU.

### Informations supplémentaires
- **Version** : 1
- **Date de création :** 14/10/2018
- **Responsable** : BARCHID Sami
