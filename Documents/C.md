Langage de programmation structuré, mais de bas niveaux, permettant de manipuler dynamiquement les espaces mémoire avec des pointeurs, offrant des types primitifs, et très performant grâce à une implémentation de ses compilateurs près du processeur.

# Table des matières #

- [Table des matières](#table-des-matières)
- [1. Historique](#1-historique)
- [2. Sources](#2-sources)
  - [2.1 Commentaires](#21-commentaires)
  - [2.2 Blocs](#22-blocs)
  - [2.3 Point d'entré](#23-point-dentré)
- [3. Processus](#3-processus)
  - [3.1 Compilation](#31-compilation)
- [4. Types](#4-types)
  - [4.1 Entiers](#41-entiers)
  - [4.2 Réels](#42-réels)
  - [4.3 Booléens](#43-booléens)
  - [4.4 Caractères](#44-caractères)
- [5. Variables](#5-variables)
  - [5.1 Pointeurs](#51-pointeurs)
  - [5.2 Tableaux](#52-tableaux)
    - [5.2.1 Chaîne de caractères](#521-chaîne-de-caractères)
- [6. Structures](#6-structures)
- [7. Structures conditionnelles](#7-structures-conditionnelles)
  - [7.1 Si](#71-si)
    - [7.1.1 Sinon](#711-sinon)
      - [7.1.1.1 Sur une ligne](#7111-sur-une-ligne)
- [8. Structure de routage](#8-structure-de-routage)
- [9. Structures itératives](#9-structures-itératives)

# 1. Historique #

En 1969, dans les laboratoires de Bell, Ken Thompson développe un système d'exploitation qui deviendra le très célèbre UNIX.

Développé en Assembleur, le système d'exploitation devient difficile à maintenir et à faire évoluer. Thompson, ne trouvant pas d'alternatives existantes viables, conçut, avec l'aide de Denis Ritchie, le langage B. Mais celui-ci n'aboutit pas convenablement pour la réécriture du système UNIX. En 1971, Denis Ritchie entreprit donc de faire évoluer le langage B, pour devenir le langage C.

![Denis Ritchie et Ken Thompson](Images/C/C01.jpg)

AT\&T, principal commanditaire des laboratoires Bell, oeuvrait dans le domaine des systèmes téléphoniques et, à l'époque, une loi lui interdisait de commercialiser autre chose. Ainsi, en 1975, le système d'exploitation UNIX complet, incluant son code source, fut distribué dans les universités à des fins éducatives.

C'est ainsi que le langage C devint l'un des plus utilisés dans le domaine des technologies de l'information.

# 2. Sources #

Le code source d'un programme en langage C est stocké dans des fichiers textes ayant, habituellement, « .c » comme extension.

## 2.1 Commentaires ##

Tout ce qui suit les caractères « // » sur une ligne est ignoré par le compilateur :

```C
// Commentaire sur une ligne.
```

Tout ce qui est encadré des balises « /* » et « */ » est aussi ignoré par le compilateur :

```C
/* Commentaire
   entre
   balises. */
```

## 2.2 Blocs ##

Un bloc d'instructions est initié par une accolade ouvrante et terminé par une accolade fermante :

```C
{ // Début du bloc d'instructions.
  // Contenu du bloc d'instructions.
} // Fin du bloc d'instructions.
```

## 2.3 Point d'entré ##

La procédure, ou fonction, identifiée « main » est le point de d'entré d'un programme en langage C :

```C
// Procédure principale.
void main() {
  // Instructions de la procédure principale.
}
```

La fonction principale permet de retourner une valeur entière au système d'exploitation :

```C
// Fonction principale.
int main() {
  // Instructions de la fonction principale.

  return 0;
}
```

La fonction principale peut aussi recevoir des paramètres :

```C
// Fonction principale avec paramètres.
int main(int argc, char *argv[]) {
  // Instructions de la fonction principale.

  return 0;
}
```

# 3. Processus #

Texte.

## 3.1 Compilation ##

Texte.

# 4. Types #

Texte.

## 4.1 Entiers ##

Texte.

## 4.2 Réels ##

Texte.

## 4.3 Booléens ##

Le langage C ne comporte pas de type booléen. Toutes les valeurs numériques autre que 0 sont considérées comme étant vraie (true). Il est par contre possible de déclarer des constantes (true) et (false) à cet effet, ou d'inclure l'en-tête contenant ces déclarations :

```C
#include <stdbool.h>
```

## 4.4 Caractères ##

Texte.

# 5. Variables #

Texte.

## 5.1 Pointeurs ##

Texte.

## 5.2 Tableaux ##

Texte.

### 5.2.1 Chaîne de caractères ###

Une chaîne de caractères est en réalité un tableau de caractères :

```C
char chaine[18] = "Bonjour le monde!";
```

Il est à noter qu'une chaîne de caractères doit toujours se terminer par le caractère « NULL », soit la valeur 0, d'ou la case supplémentaire du tableau.

# 6. Structures #

Texte.

# 7. Structures conditionnelles #

Texte.

## 7.1 Si ##

Texte.

```C
if (proposition)
  instruction();
```

Texte.

```C
if (proposition) {
  instructionA();
  instructionB();
  // ...
}
```

### 7.1.1 Sinon ###

Texte.

```C
if (proposition)
  instructionA();
else
  instructionB();
```

#### 7.1.1.1 Sur une ligne ####

Texte.

```C
(proposition) ? instructionA() : instructionB();
```

Texte.

```C
valeurA = (proposition) ? valeurB : valeurC;
```

# 8. Structure de routage #

Texte.

```C
switch (valeur) {
  case valeurA:
    instructionA();
    break;
  case valeurB:
    instructionB();
}
```

Texte.

```C
switch (valeur) {
  case valeurA:
    instructionA();
    break;
  case valeurB:
    instructionB();
    break;
  default:
    instructionC();
}
```

Texte.

```C
switch (valeur) {
  case valeurA:
    instructionA();
    break;
  case valeurB:
    instructionB();
  case valeurC:
    instructionC();
    break;
  default:
    instructionD();
}
```

# 9. Structures itératives #

Texte.

```C
while (proposition)
  instruction();
```