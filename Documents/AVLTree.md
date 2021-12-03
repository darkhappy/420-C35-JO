# Arbre binaire de recherche A.V.L.

L'arbre A.V.L. a exactement les mêmes fonctionnalités et utilités que l'arbre binaire de recherche, mais il vient palier le défaut de performance que ce dernier peut avoir.

## Performance

Puisqu'il n'est pas possible de connaître d'avance dans quel ordre les données seront ajoutées dans un arbre binaire de recherche, la performance de recherche ne peut donc pas être garantie.

Par exemple, si l'on ajoute, dans l'ordre, les données suivantes à un arbre binaire de recherche:

*[Image]*

Nous pouvons remarquer que cette structure de donnée devient inutile puisqu'une simple liste offrirait la même performance de recherche.

## Équilibre

L'arbre A.V.L. vient ajouter un mécanisme d'équilibrage afin de s'assurer de l'optimalité de la performance des recherches.

En reprenant l'exemple précédent, mais avec un Arbre A.V.L.:

*[Image]*

Nous pouvons constater la grande amélioration de la structure des données pour la recherche.

### Indice d'équilibre

Pour s'assurer de la performance de recherche, un indice d'équilibre sera calculé pour chacun des noeuds parcourus lors de l'ajout dans l'arbre.

### Rotations

...

*[Image]*