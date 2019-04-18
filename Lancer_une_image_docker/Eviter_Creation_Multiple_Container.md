<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

# Eviter la création de multiple container

<p style='text-align: justify'>
A chaque exécution de la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>, le système crée un nouveau container. Avec l'option --rm à chaque exécution de la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>, le système va supprimer l'ancien container et en créer un nouveau.
</p>

##### --rm

<p style='text-align: justify'>
Automatically remove the container when it exits
</p>

``` shell
docker run --rm $nom_image
```


---
### Documentation des commandes utilisées

<a href="https://docs.docker.com/engine/reference/commandline/run/">Run</a>

---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Lancer_une_image_docker/lancement_image_docker.md">Lancement image Docker</a>

---
###### Sylvain PRAT
