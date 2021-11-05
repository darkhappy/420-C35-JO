# Pointeurs #

Un pointeur est une variable comme une autre, à l'exception qu'elle contient une adresse de la mémoire centrale plutôt qu'une valeur.

## Déclaration ##

Le caractère '*', lors de la déclaration, permet d'indiquer que la variable est un pointeur, donc qu'elle contient une adresse de la mémoire centrale.

```c
int entier;   // Valeur entière.
int* pEntier; // Adresse en mémoire centrale où se trouve une valeur entière.
```

## Allocation ##

Les pointeurs permettent un meilleur contrôle sur la gestion de la mémoire. Mais certaines opérations, habituellement exécutées automatiquement par le langage de programmation, doivent maintenant être programmées.

### C ###

En langage C, l'instruction « malloc » permet de réserver un espace en mémoire centrale selon la taille (nombre d'octets) passée en paramètre. Cette fonction retourne l'adresse en mémoire centrale de l'espace réservé :

```c
// Allocation de 4 octets en mémoire centrale et stockage de l'adresse de cet espace dans le pointeur « pEntier ».
int* pEntier = malloc(4); 
```

*Si la taille d'un type vous est inconnue, la fonction « sizeof » permet de retourner le nombre d'octets qu'occupe le type passé en paramètre.*

### C++ ###

En langage C++, le mot-clé « new » permet de réserver un espace en mémoire centrale selon la taille du type qui le suit. De plus, puisque le lange C++ supporte le paradigme orienté objet, le constructeur est automatiquement appelé suite à l'allocation de mémoire. Et finalement, l'adresse en mémoire centrale de l'espace réservé est retournée :

```cpp
// Allocation de 4 octets en mémoire centrale, affectation de la valeur 42 dans cet espace, et stockage de l'adresse dans le pointeur « pEntier ».
int* pEntier = new int(42); 
```

## Indirection ##

Le caractère '*', lors de l'utilisation d'une variable pointeur, permet d'accéder à la valeur située à l'adresse en mémoire centrale que contient le pointeur :

```c
*pEntier = 42;
entier = *pEntier;
```

## Déréférencement ##

Il est aussi possible d'obtenir l'adresse en mémoire centrale d'une variable non pointeur :

```c
int entier = 42;
int* pEntier = &entier;
```

## Libération ##

Tout espace mémoire réservé doit aussi être libéré afin de ne pas gaspiller le précieux espace de la mémoire centrale.

### C ###

En langage C, l'instruction « free » permet de libérer un espace en mémoire centrale à l'adresse du paramètre :

```c
free(pEntier);
```

### C++ ###

En langage C++, le mot-clé « delete » permet de libérer un espace en mémoire centrale à l'adresse qui le suit :

```cpp
delete pEntier;
```

# Tableaux #

Un tableau est un segment en mémoire centrale. Et la variable d'un tableau est en réalité un pointeur à l'adresse de départ de ce segment.

```c
char chaine[7] = { 'C', 'h', 'a', 'i', 'n', 'e', '\0' };
```

En réalité, la variable « chaine » est un pointeur, et donc contient une adresse de la mémoire centrale :

*[Image]*

Et lorsque l'opérateur « [] » d'un tableau est utilisé avec un indice :

```c
char a = chaine[2];
```

Il s'agit en réalité d'un calcul d'adresse mémoire :

*[Image]*

## Instanciation ##

Puisqu'il s'agit d'un pointeur, un tableau peut donc aussi être instancié dynamiquement en mémoire :

```cpp
// int tabEntiers[10];
int* tabEntiers = new int[10];
```

## Libération ##

Afin de ne pas libérer que la première case d'un tableau, nous devons spécifier, à l'aide de l'opérateur « [] », que c'est un tableau qui est pointé en mémoire centrale :

```cpp
delete[] tabEntiers;
```
