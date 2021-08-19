# Données

Les technologies de l'information consistent principalement à générer, traiter et stocker des données.

## Binaire

La base de la logique informatique repose sur le système binaire, un système de numération à base 2.

On nomme « bit » les chiffres de cette numération, généralement représentés par 0 et 1. Et l'on nomme « octet » un groupe de 8 bits, qui consiste en l'unité de base en informatique.

L'utilisation de ce système, plutôt que le système décimal, s'explique par la facilité de représenter des données et effectuer des opérations avec l'électricité; puisque soit le courant passe (1), soit il ne passe pas (0).

## Conversions

Malgré sa base minimaliste, le fonctionnement du système binaire est très similaire à celui du système décimal.

Par exemple, le nombre décimal 12345 peut être décomposé de façon suivante :

**12345** = **1** x 10000 + **2** x 1000 + **3** x 100 + **4** x 10 + **5** x 1

Et puisqu'il s'agit d'un nombre en base 10 :

**12345** = **1** x *10<sup>4</sup>* + **2** x *10<sup>3</sup>* + **3** x *10<sup>2</sup>* + **4** x *10<sup>1</sup>* + **5** x *10<sup>0</sup>*

### Binaire à Décimal

La même logique peut être utilisée avec la base 2 afin de convertir le nombre binaire 101010 en décimal :

**101010** = **1** x *2<sup>5</sup>* + **0** x *2<sup>4</sup>* + **1** x *2<sup>3</sup>* + **0** x *2<sup>2</sup>* + **1** x *2<sup>1</sup>* + **0** x *2<sup>0</sup>* = 42

### Décimal à Binaire

Plutôt que de multiplier par la base, c'est la division entière qui est utilisée pour effectuer la conversion. Le reste à cette division est ajouté au résultat, de droite à gauche, jusqu'à ce que le nombre entier décimal soit 0 :

42 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**0**<br>
21 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**10**<br>
10 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**010**<br>
&nbsp;5 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**1010**<br>
&nbsp;2 / *2* =&nbsp;&nbsp;&nbsp;**01010**<br>
&nbsp;1 / *2* = **101010**<br>
&nbsp;0 / *2* = **101010**

## Signe

Si les valeurs entières sont stockés tels quels, sous forme binaire, en mémoire, il y a par contre une exception : les valeurs négatives, puisqu’il n’y a pas de signe dans le système binaire, que des 0 et des 1.

Le bit le plus fort est donc utilisé afin d'indiquer si la valeur est positive (0) ou négative (1). Mais cette façon de faire cause des problèmes : il y a deux 0, un positif et un négatif, et les résultats d'opérations arithmétiques ne sont plus valides lorsque des valeurs négatives sont impliquées :

&nbsp;&nbsp;&nbsp;1010 (-2)<br>
\+ 0001 ( 1)<br>
------------<br>
&nbsp;&nbsp;&nbsp;1011 (-3)

### Complément à deux

Pour pallier ces problèmes, le complément à deux est utilisé pour effectuer la négation, c'est-à-dire que tous les bits sont inversés puis 1 est ajouté. Donc, pour représenter la valeur négative « -2 », nous devons appliquer le complément à deux sur la valeur « 2 » :
