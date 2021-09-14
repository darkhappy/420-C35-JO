En programmation système, ce sont principalement des fichiers exécutables qui sont produits.

# Processus

Voici le processus, du code source à l'exécution, d'un programme exécutable :

![](Images/ASM/Executable.png)

# Formats

Chaque système d'exploitation a son propre format de fichier exécutable.

## M.Z.

Le format « Mark Zbikowski » est utilisé par le système d'exploitation DOS.

![MZ](Images/ASM/MZ.png)

*Il est aussi utilisé par Window pour encapsuler son format d'exécutable, par souci de rétrocompatibilité, d'où l'adresse du format suivant.*

## P.E.

Le format « Portable Executable » est utilisé par le système d'exploitation Windows.

![MZ](Images/ASM/PE.png)

## E.L.F.

Le format « Executable And Linkable Format » est utilisé par le système d'exploitation Linux.

*[Image]*

## Mach-O

Le format « Mach-O » est utilisé par le système d'exploitation macOS.

*[Image]*

# Chargement

Avant son exécution, le système d'exploitation charge le programme en mémoire centrale et le structure en plusieurs sections :

![](Images/ASM/MEMProgram.png)

# Exemple

Exemple d'exécution à venir suite à sa présentation au prochain cours ...