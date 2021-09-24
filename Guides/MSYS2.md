Collection d'outils et de librairies de développement.

# Télécharment

Téléchargez ![MSYS2](../Fichiers/msys2.exe)
  
# Installation

Exécutez le programme d'installation précédemment téléchargé :

![1](Images/MSYS201.png)

Cliquez sur le bouton « Suivant » :

![2](Images/MSYS202.png)

Assurez-vous que le dossier d'installation est bien « C:\msys64 » et cliquez sur le bouton « Suivant » :

![3](Images/MSYS203.png)

Cliquez sur le bouton « Suivant » et patientez durant l'installation :

![4](Images/MSYS204.png)

Assurez-vous que la case « Exécutez MSYS2 64bits maintenant » est cochée et cliquez sur le bouton « Terminer » :

![5](Images/MSYS205.png)

Si l'installation a réussi, un terminal apparaîtra :

![6](Images/MSYS206.png)

## Mise à jour

Pour mettre à jour la distribution, saisissez l'instruction suivante et appuyez sur la touche « Entrée » :

```
pacman -Suy
```

*Attention de bien respecter la casse, dont le « S » qui est majuscule.*

![7](Images/MSYS207.png)

Appuyez sur la touche « Entrée » :

![8](Images/MSYS208.png)

## Outils de développement

Pour installer le compilateur, le lieur et le débogueur, saisissez l'instruction suivante et appuyez sur la touche « Entrée » :

```
pacman -S --needed base-devel mingw-w64-x86_64-toolchain
```

*Attention de bien respecter la casse, dont le « S » qui est majuscule.*

![12](Images/MSYS212.png)

Appuyez sur la touche « Entrée » :

![13](Images/MSYS213.png)

Appuyez sur la touche « Entrée » :

![14](Images/MSYS214.png)

Appuyez sur la touche « Entrée » :

![15](Images/MSYS215.png)

## Librairie graphique

Pour installer la librairie graphique SDL2, saisissez l'instruction suivante et appuyez sur la touche « Entrée » :

```
pacman -S mingw-w64-x86_64-SDL2 mingw-w64-x86_64-SDL2_ttf mingw-w64-x86_64-SDL2_image
```

*Attention de bien respecter la casse, dont le « S » qui est majuscule.*

![16](Images/msys220.png)

Appuyez sur la touche « Entrée » :

![17](Images/msys221.png)

Saisissez l'instruction suivante pour quitter le terminal :

```
exit
```

## Configuration

Dans le menu « Démarrer » de Windows, saisissez « variable » et cliquez sur « Modifier les variables d'environnement système » :

![18](Images/MSYS216.png)

![19](Images/MSYS217.png)

![20](Images/MSYS218.png)

![21](Images/MSYS219.png)
