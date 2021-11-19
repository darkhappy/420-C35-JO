# Tri rapide

Le tri rapide pourrait être considéré comme étant une amélioration du tri par sélection. C'est-à-dire qu’une fois l’élément trouvé, celui-ci sera déplacé à sa position finale. Mais en plus, le tri rapide utilise la philosophie de diviser pour régner.

Plutôt que de trier tous les éléments afin de trouver le plus petit ou le plus grand, le tri rapide se contente de trouver un pivot dans les éléments à trier. Tous les éléments se trouvant avant le pivot doivent être plus petits et tous les éléments se trouvant après le pivot doivent être plus grands. À cette étape, l’élément du pivot sera donc à sa position finale.

Ceci fait, le tri rapide recommencera, par récursivité, les mêmes opérations, mais avec la partie de gauche et de droite du pivot. Le nombre d’éléments à trier diminue donc de plus en plus et le tri par sélection devient donc de plus en plus efficace.

Bien que la compréhension de l’efficacité du tri rapide ne soit pas évidente, son implémentation reste relativement simple si on la découpe en plusieurs étapes.

## Algorithme

- Appeler le tri rapide avec l’indice minimum et l’indice maximum, de la collection d'éléments à trier, comme paramètres.

- Initialiser une variable locale « gauche » et une variable locale « pivot » à l’indice minimum ainsi qu’une variable locale « droite » à l’indice maximum.

- Vérifier si l’élément à l’indice de gauche est supérieur à l’élément de l’indice de droite. Si c’est le cas, il faut interchanger les deux valeurs et mettre à jour le pivot. Si le pivot est égal à l’indice gauche, il faut le positionner à l’indice de droite et vice-versa.

- Suite à cette vérification, et à l’échange du pivot s’il y avait lieu, il faut mettre à jour l’indice de gauche ou de droite. Si le pivot est égal à l’indice gauche, il faut décrémenter l’indice de droite. Dans le cas contraire, il faut incrémenter l’indice gauche.

- Répéter les étapes 3 et 4 jusqu'à ce que l’indice de gauche soit égal à l’indice de droite.

- Finalement, nous devons utiliser la récursivité. Si l’indice minimum est plus petit que le pivot - 1, il faut rappeler le tri rapide avec la première partie des éléments à trier (du début jusqu'au pivot - 1). Et si l’indice maximum est plus grand que le pivot + 1, il faut rappeler le tri rapide avec la dernière partie (du pivot + 1 jusqu'à la fin).

## Implémentation

Un exemple d'implémentation du tri rapide:

```cpp
void quickSort(int iMin, int iMax) {
  int g = iMin, p = iMin, d = iMax;
  
  while (g != d) {
    if (collection[g] > collection[d]) {
      swap(collection[g], collection[d]);
      p = g + d - p;
    }

    (p == g) ? d-- : g++;    
  }
  
  if (iMin < p - 1) quickSort(iMin, p - 1);
  if (iMax > p + 1) quickSort(p + 1, iMax);  
}
```
