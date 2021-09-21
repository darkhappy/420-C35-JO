Langage de programmation structuré, mais de bas niveaux, permettant de manipuler dynamiquement les espaces mémoire avec des pointeurs, offrant des types primitifs, et très performant grâce à une implémentation de ses compilateurs près du processeur.

# Historique #

En 1969, dans les laboratoires de Bell, Ken Thompson développe un système d'exploitation qui deviendra le très célèbre UNIX.

Développé en Assembleur, le système d'exploitation devient difficile à maintenir et à faire évoluer. Thompson, ne trouvant pas d'alternatives existantes viables, conçut, avec l'aide de Denis Ritchie, le langage B. Mais celui-ci n'aboutit pas convenablement pour la réécriture du système UNIX. En 1971, Denis Ritchie entreprit donc de faire évoluer le langage B, pour devenir le langage C.

![Denis Ritchie et Ken Thompson](Images/C/C01.jpg)

AT\&T, principal commanditaire des laboratoires Bell, oeuvrait dans le domaine des systèmes téléphoniques et, à l'époque, une loi lui interdisait de commercialiser autre chose. Ainsi, en 1975, le système d'exploitation UNIX complet, incluant son code source, fut distribué dans les universités à des fins éducatives.

C'est ainsi que le langage C devint l'un des plus utilisés dans le domaine des technologies de l'information.

# Sources #

Le code source d'un programme en langage C est stocké dans des fichiers textes ayant, habituellement, « .c » comme extension.

## Commentaires ##

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

## Blocs ##

Un bloc d'instructions est initié par une accolade ouvrante et terminé par une accolade fermante :

```C
{ // Début du bloc d'instructions.
  // Contenu du bloc d'instructions.
} // Fin du bloc d'instructions.
```

## Point d'entré ##

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

# Types #

Le langage C offre quelques types primitifs :

|Type   |Langage C|Taille               |Littéral                |
|-------|---------|---------------------|------------------------|
|Entier |char     |1 octet              |42 et '*'               |
|       |short    |2 octets             |32767                   |
|       |int      |4 octets             |2147483647              |
|       |long     |8 octets             |9223372036854775807     |
|Réel   |float    |4 octets             |3.1415926               |
|       |double   |8 octets             |3.141592653589793       |

Il est possible de préciser, pour les types entiers, que les valeurs peuvent qu'être positives, permettant de représenter de plus grandes valeurs :

|Langage C     |Taille  |Litéral             |
|--------------|--------|--------------------|
|unsigned char |1 octet |255                 |
|unsigned short|2 octets|65534               |
|unsigned int  |4 octets|4294967294          |
|unsigned long |8 octets|18446744073709551614|

## Booléens ##

Le langage C ne comporte pas de type booléen. Toutes les valeurs autre que 0 sont considérées comme étant vraie (true). Il est par contre possible de déclarer des constantes (true) et (false) à cet effet, ou d'inclure l'en-tête contenant ces déclarations :

```C
#include <stdbool.h>
```

## Caractères ##

Les données étant numériques, les caractères (char) sont stockés sous forme d'entiers. C'est pour cette raison, en langage C, qu'ils doivent être encadrés par des apostrophes, afin de préciser qu'une conversion est nécessaire.

### Table ASCII

La table de conversion suivante est une norme (ASCII) utilisée depuis les premiers ordinateurs personnels.

|Valeur |Caractère|Valeur |Caractère|Valeur |Caractère|Valeur |Caractère|
|------:|---------|------:|---------|------:|---------|------:|---------|
|**0**  |NULL     |**32** |' '      |**64** |'@'      |**96** |'`'      |
|**1**  |         |**33** |'!'      |**65** |'A'      |**97** |'a'      |
|**2**  |         |**34** |'"'      |**66** |'B'      |**98** |'b'      |
|**3**  |         |**35** |'#'      |**67** |'C'      |**99** |'c'      |
|**4**  |         |**36** |'$'      |**68** |'D'      |**100**|'d'      |
|**5**  |         |**37** |'%'      |**69** |'E'      |**101**|'e'      |
|**6**  |         |**38** |'&'      |**70** |'F'      |**102**|'f'      |
|**7**  |BELL     |**39** |'''      |**71** |'G'      |**103**|'g'      |
|**8**  |BS       |**40** |'('      |**72** |'H'      |**104**|'h'      |
|**9**  |TAB      |**41** |')'      |**73** |'I'      |**105**|'i'      |
|**10** |         |**42** |'*'      |**74** |'J'      |**106**|'j'      |
|**11** |         |**43** |'+'      |**75** |'K'      |**107**|'k'      |
|**12** |         |**44** |','      |**76** |'L'      |**108**|'l'      |
|**13** |CR       |**45** |'-'      |**77** |'M'      |**109**|'m'      |
|**14** |         |**46** |'.'      |**78** |'N'      |**110**|'n'      |
|**15** |         |**47** |'/'      |**79** |'O'      |**111**|'o'      |
|**16** |         |**48** |'0'      |**80** |'P'      |**112**|'p'      |
|**17** |         |**49** |'1'      |**81** |'Q'      |**113**|'q'      |
|**18** |         |**50** |'2'      |**82** |'R'      |**114**|'r'      |
|**19** |         |**51** |'3'      |**83** |'S'      |**115**|'s'      |
|**20** |         |**52** |'4'      |**84** |'T'      |**116**|'t'      |
|**21** |         |**53** |'5'      |**85** |'U'      |**117**|'u'      |
|**22** |         |**54** |'6'      |**86** |'V'      |**118**|'v'      |
|**23** |         |**55** |'7'      |**87** |'W'      |**119**|'w'      |
|**24** |         |**56** |'8'      |**88** |'X'      |**120**|'x'      |
|**25** |         |**57** |'9'      |**89** |'Y'      |**121**|'y'      |
|**26** |         |**58** |':'      |**90** |'Z'      |**122**|'z'      |
|**27** |ESC      |**59** |';'      |**91** |'['      |**123**|'{'      |
|**28** |         |**60** |'<'      |**92** |'\'      |**124**|'|'      |
|**29** |         |**61** |'='      |**93** |']'      |**125**|'}'      |
|**30** |         |**62** |'>'      |**94** |'^'      |**126**|'~'      |
|**31** |         |**63** |'?'      |**95** |'_'      |**127**|DEL      |

# Définitions de type

L'identificateur de certains types n'est parfois pas assez révélateur au niveau du type de donnée et de sa taille. Il est possible de créer des alias de ces types :

```c
typedef char byte;
```

*Même s'il s'agit du même type de données, la taille est plus claire, et il est plus simple de différencier les valeurs entières (en utilisant « byte ») des valeurs caractères (en utilisant « char »).*

# Variables #

Les variables représentent des espaces, en mémoire centrale, afin de pouvoir y stocker et y consulter des données.

## Identificateurs

Plutôt que d'utiliser les adresses physiques de la mémoire centrale pour accéder aux données, il est possible de « nommer » les variables à l'aide d'un identificateur. Mais quelques contraintes s'appliquent à la composition de ceux-ci :

- Doivent débuter par une lettre ou le caractère '_'.
- Doivent contenir que des lettres, des chiffres, et des caractères '_'.
- Doivent être différents des mots-clés du langage C.

## Pointeurs ##

...

## Tableaux ##

...

### Chaîne de caractères ###

Une chaîne de caractères est en réalité un tableau de caractères :

```C
char chaine[18] = "Bonjour le monde!";
```

Il est à noter qu'une chaîne de caractères doit toujours se terminer par le caractère « NULL », soit la valeur 0, d'ou la case supplémentaire du tableau.

# Structures conditionnelles #

## Si ##

```C
if (proposition) {
  instructionA();
  instructionB();
  // ...
}
```

### Sinon ###

```C
if (proposition) {
  instructionA();
  instructionB();
  // ...
}
else {
  instructionC();
  instructionD();
  // ...
}
```

#### Sur une ligne ####

```C
(proposition) ? instructionA() : instructionB();
```

```C
valeurA = (proposition) ? valeurB : valeurC;
```

# Structure de routage #

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

# Structures itératives #

```C
while (proposition) {
  instructionA();
  instructionB();
  /// ...
}
```