<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

# Créer une image à partir d'un Dockerfile

<p style='text-align: justify'>
Une fois avoir terminé le Dockerfile, il faut maintenant créer une image docker à partir de se fichier.
</p>

``` shell
  docker build -t $nom_image $PATH_Dockerfile
```

<p style='text-align: justify'>
La commande build permet de créer une image docker à partir du Dockerfile. L'option -t permet de rajouter un nom à cette image.
<br>
Pour vérifier que l'image a bien été créé, la commande images permet d'afficher la totalité des images docker de la machine.
</p>

``` shell
  docker images
```



---
### Documentation des commandes utilisées

<a href="https://docs.docker.com/engine/reference/commandline/build/">Build</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/images/">Images</a><br>

---
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Dockerfile/Dockerfile.md">Dockerfile</a>

---
###### Sylvain PRAT
