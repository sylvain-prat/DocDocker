<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />  
5 Avenue Pasteur, 13100 Aix-en-Provence

***

# Transférer une image docker sans passer par Docker Hub

### 1 - Exporter vers un fichier tar
<p style='text-align: justify'>
Afin de pouvoir utiliser notre image sur une autre machine, nous devons commencer par l'exporter sous forme d'un fichier tar. Pour cela deux commandes s'offrent à nous :   
</p>

- [export](https://docs.docker.com/engine/reference/commandline/export/)
- [save](https://docs.docker.com/engine/reference/commandline/save/)

<p style='text-align: justify'>
Export permet de générer un tar à partir d'un container alors que save à partir d'une image. La commande export n'exporte pas la totalité de l'image du container (il n'importe par exemple pas CMD). <br> Je vous conseille donc d'utiliser la commande save pour éviter d'avoir à rajouter toutes les données manquantes manuellement.
<br>
</p>



``` shell
docker save -o fichierDestination.tar $image_name
```
``` shell
docker export -o fichierDestination.tar $container_name
```

<p style='text-align: justify'>
Connaitre le nom d'une image :
</p>

``` shell
  docker images
```

<p style='text-align: justify'>
Connaitre le nom d'un container :
</p>

``` shell
  docker ps -a
```

### 2 - Transmettre le fichier tar à l'autre machine


### 3 - Importer un fichier tar
<p style='text-align: justify'>

Maintenant que vous êtes sur la nouvelle machine vous n'avez plus qu'à charger la nouvelle image à partir du tar généré précedemment. Pour cela deux commandes s'offrent à nous :

- [import](https://docs.docker.com/engine/reference/commandline/import/)
- [load](https://docs.docker.com/engine/reference/commandline/load/)

La commande import va créer une nouvelle image à partir du fichier tar.
La commande load va mettre à jour ou créer une nouvelle image à partir du fichier tar. Comme export, la commande import ne va pas charger toute les données du fichier tar.<br>
Je vous conseille donc d'utiliser la commande load pour éviter d'avoir à rajouter toutes les données manquantes manuellement.
</p>

``` shell
  docker load -i fichier.tar
```

``` shell
  docker import fichier.tar
```


---
### Documentation des commandes utilisées

<a href="https://docs.docker.com/engine/reference/commandline/images/"> Images</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/ps/"> Ps</a>


<a href="https://docs.docker.com/engine/reference/commandline/export/"> Export</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/import/"> Import</a>

<a href="https://docs.docker.com/engine/reference/commandline/save/"> Save</a> <br>
<a href="https://docs.docker.com/engine/reference/commandline/load/"> Load</a>

---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Diffusion_Image_Docker/Diffusion_Image_Docker.md">Diffusion image docker</a>

---
###### Sylvain PRAT
