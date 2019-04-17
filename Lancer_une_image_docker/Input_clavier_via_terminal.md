<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

###  Input clavier via le terminal

<p style='text-align: justify'>
Pour permettre une interaction entre l'utilisateur et le programme via un terminal, il est nécessaire de rajouter les options -ti.
</p>

##### -t

<p style='text-align: justify'>
Allocate a pseudo-TTY
</p>

##### -i

<p style='text-align: justify'>
Keep STDIN open even if not attached
</p>

``` shell
docker run -ti $nom_image
```


---
### Documentation des commandes utilisées

<a href="https://docs.docker.com/engine/reference/commandline/run/">Run</a>

---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Lancer_une_image_docker/lancement_image_docker.md">Lancement image Docker</a>

---
###### Sylvain PRAT
