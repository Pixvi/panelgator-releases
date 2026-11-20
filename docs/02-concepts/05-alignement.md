# Alignement, trait de scie et rééquerrage

Trois réglages principaux influencent le calcul de votre calepinage : l'**alignement préféré**, le **trait de scie** et le **rééquerrage**.

## Alignement préféré

L'algorithme de calepinage produit uniquement des coupes traversantes selon un système de niveau. (Level)

- L0 = Panneau entier, niveau racine
- L1 = Bandes primaires issues de la première série de coupe
- L2 = Sous-bandes ou pièces issues de coupes perpendiculaires des bandes L1
- L3 = Subdivision jusqu'à libérer la pièce etc...

```
L0             L2          L2                 
   ┌────────────┬───────────┬────────────────┐
   │            │           │                │
   │            │           │                │
   │            │   L2      │         L2     │
L1 ├────────────┴────┬──────┴──────────┬─────┤
   │                 │                 │     │
   │                 │                 │     │
   │                 │   L2            │     │
L1 ├─────────────────┴────┬────────────┴─────┤
   │                      │                  │
   │                      │                  │
   │                   L3 ├──────────────────┤
   └──────────────────────┴──────────────────┘
```
Le choix de l'alignement force l'orientation des premieres coupes (L1)


### Longueur

Les bandes primaires sont **horizontales**, parallèles à la longueur du panneau. La chute est attendue en bas. C'est le mode classique pour **débiter confortablement** sur une scie à format ou une scie à panneau.

```
L0                                            
   ┌─────────────────────────────────────────┐
   │                                         │
   │                Bande A                  │
   │                                         │
L1 ├─────────────────────────────────────────┤
   │                                         │
   │                Bande B                  │
   │                                         │
L1 ├─────────────────────────────────────────┤
   │                                         │
   │                Chute                    │
   │                                         │
   └─────────────────────────────────────────┘
```

### Largeur

Les bandes primaires sont **verticales**, parallèles à la largeur du panneau. La chute est attendue à droite. 

```
L0           L1        L1                     
   ┌─────────┬─────────┬─────────────────────┐
   │         │         │                     │
   │ Bande A │ Bande B │        Chute        │
   │         │         │                     │
   │         │         │                     │
   │         │         │                     │
   │         │         │                     │
   │         │         │                     │
   │         │         │                     │
   │         │         │                     │
   │         │         │                     │
   │         │         │                     │
   └─────────┴─────────┴─────────────────────┘
```

### Optimal 

L'alignement **optimal** autorise les coupes primaires dans les deux directions. Dans la longueur et dans la largeur. Cet alignement peut produire une imbrication plus performante des pièces au détriment du confort de coupe. La chute est attendue en bas à droite.

La découpe en **mode optimal** peut nécessiter plus de manipulations de l'opérateur. De ce fait il est plutôt destiné aux **scies à panneaux** ou **CNC**

Exemple : Dans l'illustration ci-dessous la **bande B** est libérée au niveau 2 (L.2) vs. niveau 1 (L.1) avec un alignement en longueur ou en largeur.

```
L0           L1                               
   ┌─────────┬───────────────────────────────┐
   │         │                               │
   │ Bande A │           Bande B             │
   │         │                               │
   │         │                               │
   │      L2 ├───────────────────────────────┤
   │         │                               │
   │         │                               │
   │         │            Chute              │
   │         │                               │
   │         │                               │
   │         │                               │
   └─────────┴───────────────────────────────┘
```

> [!TIP]
> Panelgator compare les 3 alignements à chaque calcul et vous avertit automatiquement si un meilleur choix existe.
>
> ![avertissement automatique d'un meilleur choix d'alignement](../images/resultat-avertissement-alignement.png)



## Trait de scie

Le **trait de scie** est l'épaisseur de matière retirée par la lame entre deux pièces adjacentes sur un panneau. Il dépend de votre outillage :

- **Scie circulaire** — typiquement 2,5 à 3,5 mm
- **Scie à format** — 3 à 4 mm
- **Scie à panneaux** — 3 à 4 mm
- **CNC fraisée** — 5 à 10 mm selon la fraise

Réglage par défaut : **3 mm**, conservateur pour la plupart des configurations d'atelier.

Panelgator déduit cette valeur entre chaque pièce dans le calepinage.


## Rééquerrage

Le **rééquerrage** est une marge retirée des bords du panneau brut, pour compenser :

- Les bords abîmés ou ébréchés du transport
- Les défauts d'équerrage 
- La sécurité visuelle si vous voulez garantir un aspect impeccable des bords après débit

Réglage par défaut : **15 mm**.

Panelgator applique le rééquerrage selon le **type de panneau** :

- **Entier** ou **Chute** — sur les **4 côtés** du panneau
- **Tablette** — uniquement sur les **2 bouts** 

Vous pouvez régler la valeur entre 0 mm (aucun rééquerrage) et 100 mm (rééquerrage généreux).


## Bon à savoir

- Les paramètres de découpe sont **persistants** : ils sont conservés entre les sessions mais pas sauvegardés dans le projet `.pnlg`
- Modifier ces réglages **invalide automatiquement** le résultat de calepinage précédent. Vous devez relancer le calcul pour voir l'effet.
- Le bouton **Réinitialiser** en bas de l'onglet Réglages restaure les valeurs par défaut.

## À lire ensuite

- <!-- LINK_DISABLED: ../../05-onglet-reglages/ -->Onglet Réglages — fiche complète de tous les paramètres disponibles
- <!-- LINK_DISABLED: ../../06-onglet-resultats/ -->Onglet Résultats — visualisation et compréhension des statistiques de calepinage
