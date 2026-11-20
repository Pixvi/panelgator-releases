<p align="center">
  <img src=".github/assets/logo.png" alt="Panelgator" width="260">
</p>

<p align="center">
  <b>Calepinage automatique et feuilles de débit</b> pour l'agencement.
</p>

<p align="center">
  <a href="https://github.com/Pixvi/panelgator-releases/releases/latest"><img src="https://img.shields.io/github/v/release/Pixvi/panelgator-releases?label=version&color=e8a838" alt="Dernière version"></a>
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078d4" alt="Windows 10 | 11">
</p>

<p align="center">
  <a href="https://github.com/Pixvi/panelgator-releases/releases/latest/download/Panelgator-Setup.exe"><b>⬇&nbsp;&nbsp;Télécharger pour Windows</b></a>
</p>

<p align="center">
  <img src=".github/assets/demo.gif" alt="Démonstration de Panelgator : saisie des pièces puis calcul du calepinage" width="900">
</p>

## Installation

1. Télécharger [`Panelgator-Setup.exe`](https://github.com/Pixvi/panelgator-releases/releases/latest/download/Panelgator-Setup.exe) et le lancer.
2. Windows affiche **« Windows a protégé votre ordinateur »** : cliquer sur **Informations
   complémentaires**, puis **Exécuter quand même**.
3. Panelgator s'installe et se lance. Le raccourci est dans le menu Démarrer.

> [!NOTE]
> L'avertissement apparaît parce que l'installeur n'est pas signé par un certificat payant. Il ne
> vient que de ce dépôt. En cas de doute, ne téléchargez Panelgator que depuis la page
> [Releases](https://github.com/Pixvi/panelgator-releases/releases).

**Mises à jour** : automatiques. Panelgator télécharge la nouvelle version en arrière-plan et
propose de l'installer dès qu'elle est prête. Si on répond « Plus tard », il la repropose au
lancement suivant.

## Fonctionnalités

| | |
|---|---|
| **Import** | Fichiers `.BXF2` de Blum e-Services et `.CSV` : pas de double saisie. |
| **Stock** | Plusieurs matériaux par projet : matière, épaisseur, panneaux entiers, chutes ou tablettes, stock limité ou illimité. |
| **Chants** | Chants par côté, assignés à l'import, épaisseur déduite, longueurs totales calculées. |
| **Fil** | Sens du fil par matériau et par pièce, pièces liées pour garder la continuité du veinage. |
| **Coupe** | Lame, rééquerrage, sens de coupe selon la machine : scie à panneau, scie à format ou CNC. |
| **Export** | Feuille de débit, plans de coupe et étiquettes en `.PDF`, `.DXF` et `.CSV`. |

## Exports

<table>
  <tr>
    <td align="center"><img src=".github/assets/debit.png" alt="Feuille de débit" width="260"><br><b>Feuille de débit</b></td>
    <td align="center"><img src=".github/assets/calepinage.png" alt="Plan de coupe" width="260"><br><b>Plans de coupe</b></td>
    <td align="center"><img src=".github/assets/etiquettes.png" alt="Étiquettes" width="260"><br><b>Étiquettes</b></td>
  </tr>
</table>

## Bon à savoir

- **Windows uniquement**.
- Les projets sont des fichiers `.pnlg` : on les enregistre où on veut et on peut se les échanger.
- Aucune donnée ne quitte le PC, à part la vérification des mises à jour sur GitHub.

## À propos

Panelgator est **gratuit** et partagé tel quel, sans garantie ni support.

<p align="center"><sub>Vincent · Pixvi</sub></p>
