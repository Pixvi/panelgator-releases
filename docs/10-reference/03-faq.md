# FAQ

Réponses courtes aux questions les plus courantes.

## Prix et licence

### Combien coûte Panelgator ?

Rien. Panelgator est gratuit, sans licence ni compte. Il est partagé tel quel, sans garantie.

## Installation et mise à jour

### Sur quels systèmes Panelgator fonctionne-t-il ?

**Windows 10 et 11 (64 bits)** uniquement.


### SmartScreen affiche un avertissement à l'installation, c'est sûr ?

Oui, s'il vient de la page [Releases](https://github.com/Pixvi/panelgator-releases/releases) de ce dépôt. L'avertissement apparaît parce que l'installeur n'est pas signé par un certificat payant.

Pour continuer l'installation : cliquez sur « Informations complémentaires », puis sur « Exécuter quand même ».


### Les mises à jour sont-elles automatiques ?

Oui. Panelgator détecte les nouvelles versions au démarrage et télécharge la mise à jour en arrière-plan. Vous pouvez choisir **installer et redémarrer maintenant** ou **plus tard**. Si vous cliquez sur **plus tard** l'application vous redemandera d'installer la mise à jour au prochain démarrage.

## Projets et données

### Où sont stockés mes projets ?

Les projets enregistrés depuis Panelgator se présentent sous le format `.pnlg`. C'est un fichier autonome qui contient toute la liste de pièces et le stock du projet.
Vous pouvez le ranger où vous voulez (dossier projet local, cloud OneDrive, Dropbox, etc.), le partager, l'envoyer par e-mail etc..

### Où est stocké le stock permanent (épinglé) ?

Le stock permanent est enregistré à la fois dans le projet `.pnlg` et dans la mémoire persistante de l'application sur votre machine. Le stock permanent permet d'avoir toujours vos matériaux courants à portée de main lorsque vous démarrez un nouveau projet. Le stock du projet lui se synchronise à l'ouverture / fermeture d'un `.pnlg`.

### Mes données sont-elles envoyées sur internet ?

**Non.** Panelgator fonctionne hors-ligne. Les seules requêtes réseau sont :

- Vérification des mises à jour 
- Téléchargement des mises à jour quand une nouvelle version est disponible

Vos pièces, votre stock et vos calculs ne quittent jamais votre ordinateur.

### Puis-je travailler sans connexion internet ?

Oui, à 100 %. Une connexion est seulement utile pour recevoir les mises à jour.


## Imports et exports

### Quels formats puis-je importer ?

- **BXF2** 
- **CSV** 

### Quels formats puis-je exporter ?

- **PDF** 
- **DXF** 
- **Étiquettes** 
- **CSV** 

### Puis-je importer un fichier Excel ?

Pas directement. Convertissez d'abord votre `.xlsx` en `.csv` (Excel : *Enregistrer sous > CSV*), puis utilisez l'import CSV de Panelgator. La modale de mapping vous laisse choisir quelle colonne correspond à quoi.

## Comportement de l'application

### Pourquoi l'application ouvre plusieurs fenêtres ?

C'est volontaire : `Ctrl+N` (Nouveau projet) ouvre une nouvelle fenêtre indépendante, ce qui permet de travailler sur deux projets en parallèle (par exemple, copier-coller des pièces d'un projet à l'autre via export/import CSV intermédiaire).

### Comment changer la langue ou le thème ?

**Onglet Réglages > Général**. Langue (français / anglais), thème (clair / sombre / système), unité (mm / cm). Les choix sont persistés sur la machine.

### Pourquoi mes pièces utilisent un autre matériau que celui choisi ?

Si vous n'avez pas explicitement assigné un matériau à une pièce, Panelgator utilise le **matériau favori** du projet (étoile dorée dans le Stock). Si vous changez de favori, les pièces sans matériau explicite suivent.


## Support

### Comment signaler un problème ?

Panelgator est partagé sans support. Pour signaler un bug ou proposer une idée, ouvrez une [issue](https://github.com/Pixvi/panelgator-releases/issues) en indiquant :

- Votre version de Panelgator (Aide > À propos)
- Une description précise du problème
- Des captures d'écran si pertinent
