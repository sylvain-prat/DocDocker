<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

#  Diffuser une image Docker grâce à DockerHub

<p style='text-align: justify'>
DockerHub est une plateforme de partage d'images mise en place par Docker.
</p>

## Publier une image

<p style='text-align: justify'>
A la manière de GitHub, vous avez un système de repository pour gérer vos images. Arrivé sur le site <a href="https://hub.docker.com/">DockerHub</a> vous devrez vous créer un compte pour pouvoir publier.
</p>

#### Commit
<p style='text-align: justify'>
Avant de publier votre image vous devez la commit à partir d'un container créé par elle même
</p>

``` shell
  docker commit $container_id $nom_commit
```
<p style='text-align: justify'>
Pour connaitre le nom d'un container :
</p>

``` shell
  docker ps -a
```

#### Tag

<p style='text-align: justify'>
Le nom du commit que l'on va push doit correspondre à l'adresse de destination. Si le nom du commit n'est pas bon, on peut le renommer avec cette commande.
</p>

``` shell
  docker tag $nom_commit $nouveau_nom
```

<p style='text-align: justify'>
Habituellement, l'adresse d'une image sur DockerHub se présente sous la forme :
</p>

``` text
    nom_compte/nom_repository:nom_image
```

#### Push

On push le commit vers l'adresse de destination qui correspond au nom du commit.

``` shell
  docker push $nom_commit
```


## Récupérer une image

<p style='text-align: justify'>
Pour charger une image :
</p>

``` shell
  docker pull $adresse_image
```

<p style='text-align: justify'>
Habituellement, l'adresse d'une image sur DockerHub se présente sous la forme :
</p>

``` text
    nom_compte/nom_repository:nom_image
```

---
### Documentation des commandes utilisées


<a href="https://docs.docker.com/engine/reference/commandline/commit/">Commit</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/ps/">Ps</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/tag/">Tag</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/push/">Push</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/pull/">Pull</a><br>



---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Diffusion_Image_Docker/Diffusion_Image_Docker.md">Diffusion image docker</a>

---
###### Sylvain PRAT
