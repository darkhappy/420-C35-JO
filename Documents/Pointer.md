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

L'instruction « malloc » permet de réserver un espace en mémoire centrale selon la taille (nombre d'octets) passée en paramètre. Cette fonction retourne l'adresse en mémoire centrale de l'espace réservé :

```c
// Réservation de 4 octets en mémoire centrale et stockage de l'adresse de cet espace dans le pointeur « pEntier ».
int* pEntier = malloc(4); 
```

*Si la taille d'un type vous est inconnue, la fonction « sizeof » permet de retourner le nombre d'octets qu'occupe le type passé en paramètre.*

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

Tout espace mémoire réservé doit aussi être libéré afin de ne pas gaspiller le précieux espace de la mémoire centrale :

```c
free(pEntier);
```

# Tableaux #

Un tableau est un segment en mémoire centrale. Et la variable d'un tableau est en réalité un pointeur à l'adresse de départ de ce segment.

*[Image]*
