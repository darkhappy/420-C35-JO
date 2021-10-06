# File #

- Type : F.I.F.O. (First-In, First-Out)
- Accès : Devant et Derrière
- Fonctionnalités : Enfiler et Défiler

## Statique ##

L'implémentation statique permet d'utiliser une file dont la taille est fixe en mémoire centrale.

### UML ###

![](../Images/ArrayQueueUML.png)

### Implémentation ###

```cpp
#include <cstdlib>

template <typename T>
class ArrayQueue {
private:
  T* array;           ///< Tableau des données
  size_t arrayLength; ///< Taille du tableau
  size_t count;       ///< Nombre de données
  size_t frontIndex;  ///< Indice du devant
  
public:
  ///\param length Taille du tableau
  ArrayQueue(size_t length) {
    count = frontIndex = 0;
    array = new T[length];
    this->arrayLength = length;
  }

  ~ArrayQueue() {
    delete[] array;
  }

  ///\brief Enfiler en fin de file
  ///\param data Donnée à empiler
  void push(T data) {
    if (count < arrayLength)
      array[(frontIndex + count++) % length] = data;
  }

  ///\brief Défile en début de file
  void pop() {
    if (count) {
      frontIndex = ++frontIndex % length;
      count--;
    }
  }

  ///\brief Derrière de file
  ///\return Valeur en fin de file
  T back() {
    return (count) ? array[(frontIndex + count - 1) % length] : NULL;
  }

  ///\brief Devant de file
  ///\return Valeur en début de file
  T front() {
    return (count) ? array[frontIndex] : NULL;
  }

  ///\brief Compte de données
  ///\return Nombre de données dans la file
  size_t size() {
    return count;
  }
};
```
