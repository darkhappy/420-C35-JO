# Données

Les technologies de l'information consistent principalement à générer, traiter et stocker des données.

# Binaire

La base de la logique informatique repose sur le système binaire, un système de numération à base 2.

On nomme « bit » les chiffres de cette numération, généralement représentés par 0 et 1. Et l'on nomme « octet » un groupe de 8 bits, qui consiste en l'unité de base en informatique.

L'utilisation de ce système, plutôt que le système décimal, s'explique par la facilité de représenter des données et effectuer des opérations avec l'électricité; puisque soit le courant passe (1), soit il ne passe pas (0).

# Conversions

Malgré sa base minimaliste, le fonctionnement du système binaire est très similaire à celui du système décimal.

Par exemple, le nombre décimal 12345 peut être décomposé de façon suivante :

**12345** = **1** x 10000 + **2** x 1000 + **3** x 100 + **4** x 10 + **5** x 1

Et puisqu'il s'agit d'un nombre en base 10 :

**12345** = **1** x *10<sup>4</sup>* + **2** x *10<sup>3</sup>* + **3** x *10<sup>2</sup>* + **4** x *10<sup>1</sup>* + **5** x *10<sup>0</sup>*

## Binaire à Décimal

La même logique peut être utilisée avec la base 2 afin de convertir le nombre binaire 101010 en décimal :

**101010** = **1** x *2<sup>5</sup>* + **0** x *2<sup>4</sup>* + **1** x *2<sup>3</sup>* + **0** x *2<sup>2</sup>* + **1** x *2<sup>1</sup>* + **0** x *2<sup>0</sup>* = 42

## Décimal à Binaire

Plutôt que de multiplier par la base, c'est la division entière qui est utilisée pour effectuer la conversion. Le reste à cette division est ajouté au résultat, de droite à gauche, jusqu'à ce que le nombre entier décimal soit 0 :

42 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**0**<br>
21 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**10**<br>
10 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**010**<br>
&nbsp;5 / *2* =&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**1010**<br>
&nbsp;2 / *2* =&nbsp;&nbsp;&nbsp;**01010**<br>
&nbsp;1 / *2* = **101010**<br>
&nbsp;0 / *2* = **101010**

# Signe

Si les valeurs entières sont stockés tels quels, sous forme binaire, en mémoire, il y a par contre une exception : les valeurs négatives, puisqu’il n’y a pas de signe dans le système binaire, que des 0 et des 1.

Le bit le plus fort est donc utilisé afin d'indiquer si la valeur est positive (0) ou négative (1). Mais cette façon de faire cause des problèmes : il y a deux 0, un positif et un négatif, et les résultats d'opérations arithmétiques ne sont plus valides lorsque des valeurs négatives sont impliquées :

&nbsp;&nbsp;&nbsp;1010 (-2)<br>
\+ 0001 ( 1)<br>
------------<br>
&nbsp;&nbsp;&nbsp;1011 (<span style="color:red">-3</span>)

## Complément à deux

Pour pallier ces problèmes, le complément à deux est utilisé pour effectuer la négation, c'est-à-dire que tous les bits sont inversés puis 1 est ajouté. Donc, pour représenter la valeur négative « -2 », nous devons appliquer le complément à deux sur la valeur « 2 » :

0010 (2) --[ inversion de tous les bits ]--> 1101 --[ ajout de 1 ]--> 1110 (-2)

Donc chaque fois que le bit le plus fort est 1, c'est que la valeur est encodée avec le complément à deux :

&nbsp;&nbsp;&nbsp;1110 (-2)<br>
\+ 0001 ( 1)<br>
------------<br>
&nbsp;&nbsp;&nbsp;1111 (<span style="color:green">-1</span>)

# Plage

L'unité de base en informatique est l'octet, mais il est possible d'utiliser plusieurs octets afin de représenter une valeur entière.

L'une des utilités des types de données, des langages de programmation, est d'indiquer l'espace nécessaire en mémoire centrale afin de stocker nos valeurs. Mais afin d'être optimal en utilisant le moins d'espace possible, il est nécessaire de faire les bons choix. Et pour ce faire, il faut nécessairement connaître les plages de valeurs de chacun des types de données.

Plutôt que d'apprendre inutilement par coeur toutes ces plages de valeurs, il est préférable de savoir comment les calculer. Pour ce faire, il suffit d'utiliser la base (2) et de l'élever selon le nombre de bits du type de données :

&nbsp;*2*<sup>**8**</sup> = 256, donc une plage de valeur entre **0** et **255** inclusivement.<br>
*2*<sup>**16**</sup> = 65 536, donc une plage de valeur entre **0** et **65 535** inclusivement.<br>
*2*<sup>**32**</sup> = 4 294 967 296, donc une plage de valeur entre **0** et **4 294 967 295** inclusivement.<br>
*2*<sup>**64**</sup> = 18 446 744 073 709 551 616, donc une plage de valeur entre **0** et **18 446 744 073 709 551 615** inclusivement.

## Signe

Les plages ci-hautes sont valides que pour des valeurs entières dites « non signées ». Puisque le bit le plus fort est utilisé pour les valeurs entières signées, la plage de valeur est donc affecté :

&nbsp;*2*<sup>**7**</sup> = 128, donc une plage de valeur entre **-128** et **127** inclusivement.<br>
*2*<sup>**15**</sup> = 32 768, donc une plage de valeur entre **-32 768** et **32 767** inclusivement.<br>
*2*<sup>**31**</sup> = 2 147 483 648, donc une plage de valeur entre **-2 147 483 648** et **2 147 483 647** inclusivement.<br>
*2*<sup>**63**</sup> = 9 223 372 036 854 775 808, donc une plage de valeur entre **-9 223 372 036 854 775 808** et **9 223 372 036 854 775 807** inclusivement.

# Représentations

Puisque tout est numérique, sous forme binaire, il n'est pas possible pour un ordinateur de représenter autre chose que des valeurs entières. Il n’est donc pas possible de différencier un booléen, un caractère ou un réel d’un entier. Donc, l'autre utilité des types de données, des langages de programmation, est d'indiquer comment interpréter les valeurs entières.

## Booléen

Bien que le système binaire soit parfaitement approprié pour ce type de données, il n'y a pas de valeur « vraie (true) » et « fausse (false) ». Plutôt, la valeur 0 permet de représenter « false », et toutes les autres valeurs représentent « true ».

## Caractère

Les caractères non plus ne sont pas des valeurs. Des tables sont plutôt utilisées, selon la langue ou les caractères à utiliser, afin d'associer chaque caractère à une valeur entière. La première, et plus connue, la table « ASCII » :

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

### Chaîne de caractères

Une chaîne de caractères n’est qu’en réalité une suite de caractères en mémoire.

## Réel

La représentation des réels est un peu plus particulière et utilise, à la base, une norme « IEEE », principalement la 754.

La plupart des langages de programmation comportent plusieurs types de réels, habituellement à simple précision (environ 7 chiffres après la virgule) :
