# Pointeurs #

Un pointeur est une variable comme une autre, à l'exception qu'elle contient une adresse de la mémoire centrale plutôt qu'une valeur.

## Déclaration ##

Le caractère '*', lors de la déclaration, permet d'indiquer que la variable est un pointeur, donc qu'elle contient une adresse de la mémoire centrale.

```c
int entier;   // Valeur entière.
int* pEntier; // Adresse en mémoire centrale où se trouve une valeur entière.
```

## Instanciation ##

Les pointeurs permettent un meilleur contrôle sur la gestion de la mémoire. Mais certaines opérations, habituellement exécutées automatiquement par le langage de programmation, doivent maintenant être programmées.

L'instruction « malloc » permet de réserver un espace en mémoire centrale selon la taille (nombre d'octets) passé en paramètre. Cette fonctione retourne l'adresse en mémoire centrale de l'espace réservé :

```c
int* pEntier = malloc(4); // Réservation de 4 octets en mémoire centrale et stockage de l'adresse de cet espace dans le pointeur « pEntier ».
```

*Si la taille d'un type vous est inconnu, la fonction « sizeof » permet de retourner le nombre d'octet qu'occupe le type passé en paramètre.*

## Affectation ##

Le caractère '*', lors de l'utilisation d'une variable pointeur, permet d'accéder à l'adresse en mémoire centrale :

```c
*pEntier = 42;
entier = *pEntier;
```

## Libération ##

Tout espace mémoire réservé, doit aussi être libéré afin de ne pas gaspiller le précieux espace de la mémoire centrale :

```c
free(pEntier);
```

# Tableaux #

Un tableau est un segment en mémoire centrale. Et la variable d'un tableau est en réalité un pointeur à l'adresse de départ de ce segment.

*[Image]*

## Chaîne de caractères ##

Une chaîne de caractères est en réalité un tableau de caractères :

```C
char chaine[18] = "Bonjour le monde!";
```

Il est à noter qu'une chaîne de caractères doit toujours se terminer par le caractère « NULL », soit la valeur 0, d'ou la case supplémentaire du tableau.