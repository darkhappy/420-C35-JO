Notions de base en sécurité logicielle.

# Vulnérabilité

Lors de l'implémentation d'un programme, des failles peuvent être créées, le rendant vulnérable aux exploits.

## Débordement

Les langages de bas niveau laissent beaucoup de latitude au niveau de l'utilisation de la mémoire à l'aide de pointeurs. Mais une irresponsabilité ou une méconnaissance du fonctionnement de l'exécution d'un programme peut engendrer des vulnérabilités.

### Tampon

...

## Pile d'exécution

En 1988, le ver « Morris » est l'un des premiers virus capables de se répliquer par lui-même via l'Internet. L'une des vulnérabilités utilisées consiste à exploiter la pile d'exécution.

...

# Virus

En 1949, Jonh Von Neumann publie un essai « Theory of self-reproducing automata » démontrant comment un programme informatique peut être conçu afin de se répliquer par lui-même.

## Infection

Au niveau logiciel, il y a plusieurs façons d'infecter un programme exécutable :

### Jointure

La charge utile peut être jointe à un fichier exécutable.

*[Image]*

Cette technique est peu utilisée puisque la taille du fichier doit être modifiée, le rendant ainsi beaucoup plus facile à détecter par les logiciels antivirus.

### Cavité

Les formats d'exécutables et les compilateurs laissent certains espaces libres, sans données, ce que l'on nomme des cavités :

*[Image]*

La charge utile peut être stockée dans l'une de ces cavités, la rendant beaucoup plus difficile à détecter.

## Exécution

La charge utile est, la majorité du temps, déclenchée automatiquement, de façon transparente, lors de l'exécution du programme infecté.

### Point d'entrée

*[Image]*

### Détournement

*[Image]*

## Obfuscation

Des techniques peuvent être ajoutées afin de rendre plus difficiles la détection, la compréhension, et l'analyse dynamique de la charge utile.

### Emballeur

La plupart des maliciels modernes utilisent un emballeur (packer), c'est-à-dire que la charge utile est encodée / compressée / cryptée, empêchant l'analyser de ses instructions sans préalablement les décoder.

# Glossaire

|Terme|Description|
|---|---|
|Certificat|Mécanisme cryptographique employé pour vérifier l'authenticité et l'intégrité d'un logiciel.|
|Charge utile (Payload)|Partie active d'un logiciel malveillant.|
|Cyberattaque|Recours à des techniques électroniques visant à perturber, manipuler, détruire ou scruter clandestinement un système informatique, un réseau ou un dispositif.|
|Cybermenace|Entité malveillante profitant d’une vulnérabilité connue en vue d’exploiter un système informatique, un réseau ou un dispositif.|
|Exploit|Une manière définie de transgresser la sécurité d'un système informatique, un réseau ou un dispositif, par l'entremise d'une vulnérabilité.|
|Jour zéro (Zeroday)|Vulnérabilité logicielle dont l’existence n’est pas encore connue du fournisseur et qui n’est donc pas atténuée. Un exploit de jour zéro désigne une attaque qui exploite une vulnérabilité de jour zéro.|
|Maliciel (Malware)|Logiciel malveillant conçu pour infiltrer un système informatique, un réseau ou un dispositif.|
|Pirate (Hacker)|Personne qui utilise des ordinateurs pour accéder à d’autres système informatique, réseau ou dispositif, sans en avoir la permission.|
|Virus|Programme informatique qui se propage en se copiant par lui-même à l’insu de l’utilisateur.|
|Vulnérabilité|Défectuosité ou lacune inhérente à la conception ou à la mise en œuvre d’un système d’information, ou à son environnement, qui pourrait être exploitée.|