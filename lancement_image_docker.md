<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***
# Exécution d'une image docker
<p style='text-align: justify'>
Une fois l'image Docker créé, il ne nous reste plus qu'à l'exécuter pour lancer son contenu. Pour exécuter un image docker, il suffit d'utiliser la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>. Après exécution de la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>, le système va créer un container basé sur l'image passé en paramètre de la commande.
</p>

``` shell
docker run $nom_image
```

<p style='text-align: justify'>
Vu que notre programme docker s'exécute dans un container, il est totalement isolé du système. Pour pouvoir intéragir avec notre programme, nous allons devoir ajouter des options lors du lancement du programme.
</p>

###  Input clavier via le terminal

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


###  Interface Graphique
#### Windows
#### Linux

---
### Documentation des commandes utilisés

<a href="https://docs.docker.com/engine/reference/commandline/run/">Run</a>

---
###### Sylvain PRAT
