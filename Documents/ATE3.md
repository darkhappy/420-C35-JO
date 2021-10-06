# Atelier 3 #

Une expression arithmétique est composée d'opérandes et d'opérateurs exprimés de façon infixe. Mais pour évaluer une expression arithmétique, la priorité des opérateurs doit être respectée.

## Priorités ##

0. ( et )
1. \+ et -
2. \* / et %
   
## Infixe à Postfixe ##

Les programmes informatiques, dont les compilateurs, sont confrontés à l'évaluation d'expressions arithmétiques. Afin de simplifier la tâche, les expressions sont d'abord exprimées de façon postfixe.

- Un opérande est directement ajouté à la file postfixe.
- Une parenthèse ouvrante est empilée sur la pile d'opérateurs.
- Une parenthèse fermante dépile les opérateurs, dans la file postfix, jusqu'à une parenthèse ouvrante, aussi dépilée.
- Un opérateur est empilé après avoir dépilé, dans la file postfixe, ceux ayant une priorité supérieure ou égale.
- Lorsque la file infixe est vide, dépiler, dans la file postfixe, jusqu'à ce que la pile soit vide.
  
## Postfixe à Résultat ##

Les expressions postfixe permettent d'évaluer le résultat en respectant les priorités des opérateurs.

- Un opérande est directement empilé dans la pile d'opérandes.
- Un opérateur est appliqué aux deux opérandes dépilés et le résultat empilé.
- Suite à l'évaluation, le dessus de la pile consistera au résultat.

## Projet ##

Le projet devra inclure la classe pour utiliser des chaînes de caractères, la classe pour utiliser des piles statiques, et la classe pour utiliser des files statiques :

```cpp
#include <string>
#include "ArrayStack.hpp"
#include "ArrayQueue.hpp"

using namespace std;

///\brief Transformation d'une expression infixe en expression postfixe.
///\param expressionQueue File contenant les opérandes et des opérateurs de l'expression infixe.
///\return File de l'expression postfixe.
ArrayQueue<string>* infixToPostfix(ArrayQueue<string>* expressionQueue) {
  // TODO : Implémentation ...
}

///\brief Calcul du résultat d'un expression postfixe.
///\param postfixQueue File contenant les opérandes et des opérateurs de l'expression postfixe.
///\return Résultat de l'expression postfixe.
int postfixToResult(ArrayQueue<string>* postfixQueue) {
  // TODO: Implémentation ...
}

///\brief Fonction principale.
///\return Code de terminaison de programme.
int main() {
  // TODO : Déclaration et instanciation de la file infixe.
  // TODO : Enfilement des opérandes et des opérateurs de l'expression infixe.

  // TODO : Appel des fonction pour transformer l'expression et calculer le résultat.

  return 0;
}
```

## Conversion ##

Des fonctions spéciales permettent de passer d'un entier à une chaîne de caractères et vice-versa :

```cpp
int entier;
string chaineCaracteres = "42";

entier = stoi(chaineCaracteres);      // Conversion d'une chaîne de caractères vers un entier.
chaineCaracteres = to_string(entier); // Conversion d'un entier vers une chaîne de caractères.
```

## Résultat ##

Le programme doit afficher les résultats sous la forme suivante :

```
Infix      : 1+2*(5+10)+11
Postfix    : 12510+*+11+
Evaluation : 42
```

## Barème ##

Infixe à Postfixe&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; / 7<br>
Postfixe à Résultat&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; / 3<br>
Affichage&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; / 1<br>

**Total&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; / 11**

*\* Les expressions utilisées seront toujours valides.*<br>
*\*\* Les opérandes utilisés dans l'expression de départ seront toujours positifs.*<br>
*\*\*\* Le nombre d'opérandes, d'opérateurs et de parenthèses total ne dépassera pas 25.*
