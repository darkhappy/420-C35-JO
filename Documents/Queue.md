# File #

- Type : F.I.F.O. (First-In, First-Out)
- Accès : Devant et Derrière
- Fonctionnalités : Enfiler et Défiler

## Dynamique ##

L'implémentation dynamique permet d'utiliser une file sans limitation de taille puisque les données sont dynamiquement allouées et libérées en mémoire centrale.

### UML ###

![](Images/CPP/QueueUML.png)

### Implémentation ###

```cpp
#include <cstdlib>
#include "SLNode.hpp"

template <typename T>
class Queue {
private:
  size_t count;     ///< Nombre de données
  SLNode<T>* first; ///< Pointeur sur le premier noeud
  SLNode<T>* last;  ///< Pointeur sur le dernier noeud

public:
  Queue() {
    count = 0;
    first = last = nullptr;
  }

  ~Queue() {
    while (count)
      pop();
  }

  ///\brief Enfiler à la fin de la file
  ///\param data Donnée à enfiler
  void push(T data) {
    if (count)
      last = last->next = new SLNode<T>(data, nullptr);
    else
      first = last = new SLNode<T>(data, nullptr);

    count++;
  }

  ///\brief Défiler au début de la file
  void pop() {
    if (count) {
      SLNode<T>* toDelete = first;
      first = first->next;
      delete toDelete;

      count--;
    }
  }

  ///\brief Derrière de la file
  ///\return Valeur à la fin de la file
  T back() {
    return (count) ? last->data : NULL;
  }

  ///\brief Devant de la file
  ///\return Valeur au devant de la file
  T front() {
    return (count) ? first->data : NULL;
  }

  ///\brief Compte de données
  ///\return Nombre de données dans la file
  size_t size() {
    return count;
  }
};
```
