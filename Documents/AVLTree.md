# Arbre binaire de recherche A.V.L.

L'arbre A.V.L. a exactement les mêmes fonctionnalités et utilités que l'arbre binaire de recherche, mais il vient pallier le défaut de performance que ce dernier peut avoir.

## Performance

Puisqu'il n'est pas possible de connaître d'avance dans quel ordre les données seront ajoutées dans un arbre binaire de recherche, la performance de recherche ne peut donc pas être garantie.

Par exemple, si l'on ajoute les mêmes données, dans le même ordre, dans les deux arbres:

![Arbre binaire de recherche vs Arbre A.V.L.](Images/BSTvsAVL.png)

Nous pouvons facilement déduire quelle structure offrira la meilleure performance de recherche.

## Équilibre

L'arbre A.V.L. vient donc ajouter un mécanisme d'équilibrage à l'arbre binaire de recherche afin de s'assurer, en tout temps, de l'optimalité de la performance des recherches.

### Rotations

L'équilibrage se fait via des rotations sur des noeuds.

![Rotation](Images/NodeRotation.png)

Pour une rotation vers la gauche à partir du noeud (A):

- L’enfant de droite (N) devient la nouvelle racine.
- L’enfant de gauche (G), de la nouvelle racine (N), devient l’enfant de droite de l’ancienne racine (A).
- L’ancienne racine (A) devient l’enfant de gauche de la nouvelle racine (N).

### Indice d'équilibre

Pour s'assurer de la performance de recherche, un indice d'équilibre sera calculé pour chacun des noeuds parcourus lors de l'ajout dans l'arbre:

```
Indice d'équilibre = Hauteur du sous-arbre de droite - Hauteur du sous-arbre de gauche
```

Et selon certains résultats, des opérations devront être effectuées:

- (-2): Rotation vers la droite
- (2): Rotation vers la gauche

#### Exception

Il y a une exception à gérer dans deux contextes bien précis:

- Indice d'équilibre (-2) et indice d'équilibre de l'enfant (1): Double-rotation gauche-droite.
- Indice d'équilibre (2) et indice d'équilibre de l'enfant (-1): Double-rotation droite-gauche.
