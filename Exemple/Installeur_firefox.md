<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

---

# Installeur de Firefox Docker
<p style='text-align: justify'>
Voici un Installeur de l'image docker firefox. Cet installeur permet de créer/mettre à jour une image docker de firefox et de le lancer sans que l'utilisateur n'est besoin d'utiliser un terminal.
</p>

### Windows

<p style='text-align: justify'>
 Prérequis :
</p>

 - Docker installé sur la machine
 -  Xming Serv 0.0 lancé


<p style='text-align: justify'>
Arborescence :
</p>

``` text
InstalleurFirefox/
          firefox.tar
          ip.txt
          firefox.exe
```

<p style='text-align: justify'>
firefox.tar permet de créer/mettre à jour l'image docker de firefox.
<br>
<br>
ip.txt est un fichier de config qui contient l'ip de l'utilisateur. L'utilisateur doit lui même écrire son ip dans le fichier de config.
<br>
<br>
firefox.exe est un exécutable d'un programme C qui met à jour l'image et la lance dans un container.

<br>
<br>

firefox.c
</p>



``` C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#define TAILLE_MAX 20

int main(int argc, char *argv[])
{

	//initialisation de l'image docker
    system("docker load -i firefox.tar");

    FILE* fichier = NULL;
    char chaine[TAILLE_MAX] = "";

    fichier = fopen("./ip.txt", "r");

    if (fichier != NULL)
    {
		//récupération de l'ip écrite dans ip.txt
        fgets(chaine, TAILLE_MAX, fichier);
		char premierepart[] = "docker run --rm -e DISPLAY=";
		char deuxiemepart[] = ":0.0 firefox";
		strcat(premierepart, chaine);
		strcat(premierepart, deuxiemepart);

		//Création du container
		system(premierepart);
        fclose(fichier);
    }



    return 0;
}
```

---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Exemple/Exemple.md">Exemple</a>

---
###### Sylvain PRAT
