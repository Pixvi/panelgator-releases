# Projet, groupe et pièces

Panelgator organise votre projet selon une hiérarchie simple : un **projet** contient un ou plusieurs **groupes**, chaque groupe contient une ou plusieurs **pièces**.

## Le projet

Un projet rassemble l'ensemble du débit d'un chantier. Vous pouvez le sauvegarder dans un fichier `.pnlg` et le rouvrir plus tard depuis n'importe quel poste équipé de Panelgator.

Il contient :
- les groupes
- les pièces
- le stock.

Le projet a un **nom** (modifiable directement dans la barre de titre) qui se retrouve dans tous les exports (PDF, DXF, étiquettes).

## Le groupe

Un groupe représente un meuble, un élément, ou tout ensemble cohérent de pièces.

Chaque groupe a :

- **Un nom** (libre, vous y mettez ce que vous voulez)
- **Des dimensions d'encombrement** facultatives (Hauteur × Largeur × Profondeur en mm) — utiles pour vérifier la cohérence des pièces qui le composent
- **Un multiplicateur** (× 1 par défaut) — multiplie toutes les pièces du groupe par ce nombre.

Les groupes sont facultatifs, vous pouvez créer des pièces sans groupe. Leur fonction est de structurer la liste de débit et d'organiser les exports selon le tri choisi. Voir <!-- LINK_DISABLED: ../../08-exports/02-pdf/#groupement-de-la-feuille-de-d%C3%A9bit -->Groupement de la feuille de débit.

### Exemple concret

Vous avez 3 caissons identiques à fabriquer. Au lieu de saisir 3 fois les mêmes pièces, vous créez **un seul groupe** *Caisson* avec multiplicateur **× 3**. Panelgator multiplie automatiquement chaque pièce du groupe par 3 dans le calepinage.

## La pièce

Une pièce correspond à un panneau individuel à découper. Elle a les caractéristiques suivantes :

- **Étiquette** — « Côté gauche », « Étagère », « Porte »…
- **Longueur × Largeur** — la longueur est toujours la dimension la plus grande
- **Quantité** — nombre d'unités de la pièce
- **Matériau** — référence à un matériau défini dans l'onglet Stock
- **Sens du fil** — orientation du veinage de la pièce, parallèle à sa longueur ou à sa largeur (voir [Sens du fil et chants](../02-concepts/03-fil-chants.md))
- **Chants plaqués** — quels côtés portent un chant collé (voir [Sens du fil et chants](../02-concepts/03-fil-chants.md))
- **Type** — catégorie de pièce (Corps, Façade, Tiroir…), utile pour filtrer (voir [Types de pièces](../02-concepts/02-types-pieces.md))
- **Remarque** — note libre

> [!NOTE]
> - Une pièce valide contient au minimum une étiquette, ses dimensions et une quantité.
> - L'épaisseur d'une pièce est définie par le matériau de stock qui lui est attribué.

## Hiérarchie en pratique

```
Projet « Cuisine Dupont »
├── Groupe « Caisson bas A » (× 3)
│   ├── Côté gauche       720 × 580
│   ├── Côté droit        720 × 580
│   ├── Dessus            596 × 580
│   ├── Dessous           596 × 580
│   ├── Dos               712 × 580
│   └── Étagère réglable  592 × 568   (× 2)
│
├── Groupe « Colonne four » (× 1)
│   ├── Côté gauche       2200 × 580
│   ├── Côté droit        2200 × 580
│   └── ...
│
└── Groupe « Façades » (× 1)
    ├── Porte             715 × 396   (× 6)
    └── Façade tiroir     296 × 568   (× 9)
```

Au calcul, Panelgator applique le multiplicateur de chaque groupe et place automatiquement toutes les pièces résultantes sur les panneaux du Stock.

Exemple : le groupe « Caisson bas A » (× 3) contient 7 pièces = 21 pièces à placer.

## Bon à savoir

- Vous pouvez **filtrer** la liste de pièces par texte (recherche dans étiquette + nom de groupe)
- Vous pouvez sélectionner plusieurs pièces et leur appliquer une <!-- LINK_DISABLED: ../../03-onglet-pieces/04-actions-masse/ -->action en masse (changer le matériau, le sens du fil, les chants, les supprimer…)
- Augmenter la **quantité** d'une pièce existante évite de la recréer si elle est strictement identique
- Les champs numériques acceptent des **expressions mathématiques**. Tapez `2800-2*19` pour obtenir 2762.

## À lire ensuite

- [Types de pièces](../02-concepts/02-types-pieces.md) — l'attribut catégorie et son utilisation
- [Sens du fil et chants](../02-concepts/03-fil-chants.md) — comment indiquer le veinage et les chants visibles
- [Stock et matériaux](../02-concepts/04-stock.md) — comment déclarer vos panneaux disponibles
