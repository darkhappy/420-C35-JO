Les normes de programmation de ce document doivent être respectées dans tous les travaux.

# Table des matières

- [Table des matières](#table-des-matières)
  - [Inclusions](#inclusions)
  - [Identification](#identification)
    - [Constante](#constante)
    - [Variables](#variables)
    - [Structure](#structure)
  - [Indentation](#indentation)
  - [Pléonasmes](#pléonasmes)
    - [Structure conditionnelle](#structure-conditionnelle)
    - [Structure répétitive](#structure-répétitive)
  - [Aération](#aération)
  - [Commentaires](#commentaires)

## Inclusions ##

Limiter les inclusions à ce qui est nécessaire au code présent dans le fichier :

```c
#include <stdio.h>
// ^^^^^^^^^^^^^^^ Ne devrait pas être présent puisqu'inutilisé.

int main() {
  return 0;
}
```

## Identification ##

Les identificateurs de constante et variable doivent être significatifs.

### Constante ###

Les caractères des identificateurs de constantes doivent tous être majuscules :

```c
#define BLANC 0
#define NOIR 1
```

### Variables ###

Les identificateurs de variables doivent utiliser la casse de chameau, c'est-à-dire commencer par un caractère minuscule, et utiliser un caractère majuscule pour commencer les mots suivants :

```c
int identificateurDeVariableEntiere = 42;
```

### Structure ###

Les identificateurs de structure doivent aussi utiliser la casse de chameau, mais débuter par un caractère majuscule :

```c
struct Position {
  int x, y;
};
```

## Indentation ##

Il doit y avoir une indentation suite aux accolades ouvrantes, aux modificateurs d'accès, aux if, aux else, aux while, aux for et aux case :

```cpp
class Classe {
public:
  void methode(int valeurEntiere) {
    switch(valeurEntiere) {
      default:
        for (int i = 0; i < 1000; i++)
          if (valeurEntiere < 42)
            valeurEntiere++;
          else
            valeurEntiere--;          
        break;
    }
  }
};
```

## Pléonasmes ##

Quelques pléonasmes de programmeur à éviter :

### Structure conditionnelle

```c
// if (proposition == true)
if (proposition)
```

*Puisque les instructions d'une structure conditionnelle sont exécutées si la proposition est vraie.*

```c
// if (compte != 0)
if (compte)
```

*Puisque la valeur 0 représente faux, tandis que toutes autres valeurs représentent vraie.*

```c
/* 
if (proposition)
  variable = true;
else
  variable = false;
*/
variable = proposition;
```

*Puisqu'une proposition est toujours de type booléen.*

### Structure répétitive

```c
/*
int iterateur = 0;
while (iterateur < compte) {
  // Instructions
  iterateur++;
}
*/
for (int iterateur = 0; iterateur < compte; iterateur++) {
  // Instructions
}
```
*Puisque le nombre d'itérations est connu et qu'il est préférable d'avoir une variable locale à la structure répétitive.*

## Aération ##

Les gros morceaux de code doivent être séparés en paragraphes afin d'être plus agréables à lire.

Tous les opérateurs, outre les opérateurs unaires, doivent être précédés et suivis d'un espace.

## Commentaires ##

Les morceaux de code non triviaux ou redondants doivent être commentés afin d'expliquer leur algorithme.
