<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

# Créer un Dockerfile

#### FROM
<p style='text-align: justify'>
Permet d'importer une image déjà existante. Sur le site <a href="https://hub.docker.com/">DockerHub</a>, il existe une multitude d'image docker publié par la communauté et même des images officielles. Par exemple Python, Microsoft, Oracle publient leurs propres images pour faciliter le développement docker.
</p>

``` text
  FROM $adresse_image
```

#### RUN

<p style='text-align: justify'>
Si votre programme nécessite des installations de package, il suffit de mettre la commande pour les installer juste après RUN.
</p>


``` text
  RUN $commande
```

#### ADD/COPY

<p style='text-align: justify'>
Il faut maintenant ajouter tous les fichiers nécessaire au fonctionnement de l'application.
COPY permet de copier des fichiers, répertoires en locals et de les ajouter au container. ADD fais la même chose que COPY sauf qu'il peut aussi prendre une url en paramètre et ainsi télécharger les fichiers de l'url pour ensuite les ajouter au container. ADD décompresse également les fichiers tar qui lui sont passés en paramètre.
</p>

``` text
  COPY $adresse_fichier ...      $adresse_destination_dans_container
```

``` text
  ADD $adresse_fichier ...    $adresse_destination_dans_container
```

``` text
  ADD $url  $adresse_destination_dans_container
```

<p style='text-align: justify'>
On peut définir un répertoire de travail pour ADD et COPY dans le container avec WORKDIR
</p>

``` text
  WORKDIR $PATH
```

#### CMD

<p style='text-align: justify'>
CMD permet d'affecter une commande au container qui sera exécuté au moment de la création du container. Il ne peut y avoir qu'une commande pour un container, docker ne prendra donc en compte que le dernier CMD du Dockerfile.
</p>

``` text
  CMD ["param1","param2", ...]
```

<p style='text-align: justify'>
Pour la commande :
</p>

``` shell
  python app.py param
```

``` text
  CMD ["python","app.py","param"]
```


---
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Dockerfile/Dockerfile.md">Dockerfile</a>

---
###### Sylvain PRAT
