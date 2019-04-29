<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***
# Exécution d'une image docker
<p style='text-align: justify'>
Une fois l'image Docker créée, il ne nous reste plus qu'à l'exécuter pour lancer son contenu. Pour exécuter une image docker, il suffit d'utiliser la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>. Après exécution de la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>, le système va créer un container basé sur l'image passée en paramètre de la commande.
</p>

``` shell
docker run $nom_image
```

<p style='text-align: justify'>
Vu que notre programme docker s'exécute dans un container, il est totalement isolé du système. Pour pouvoir intéragir avec notre programme, nous allons devoir ajouter des options lors du lancement du programme.
</p>

---

## Sommaire

- #### <a href='https://github.com/sylvain-prat/DocDocker/blob/master/Lancer_une_image_docker/Input_clavier_via_terminal.md'>Input clavier via le terminal</a>
- #### <a href='https://github.com/sylvain-prat/DocDocker/blob/master/Lancer_une_image_docker/Eviter_Creation_Multiple_Container.md'>Eviter la création de multiple container</a>
- #### <a href='https://github.com/sylvain-prat/DocDocker/blob/master/Lancer_une_image_docker/Interface_Graphique.md'>Interface Graphique</a>



---
### Documentation des commandes utilisées

<a href="https://docs.docker.com/engine/reference/commandline/run/">Run</a>

---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>

---
###### Sylvain PRAT
