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

---

- <a href='#ICT'>Input clavier via le terminal</a>
- <a href='#ECMC'>Eviter la création de multiple container</a>
- <a href='#IG'>Interface Graphique</a>
- <a href='#DS'>Diffuser du son</a>

---
<div id="ICT"></div>

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
 <div id="ECMC"></div>

### Eviter la création de multiple container

<p style='text-align: justify'>
A chaque exécution de la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>, le système crée un nouveau container. Avec l'option --rm à chaque exécution de la commande <a href="https://docs.docker.com/engine/reference/commandline/run/">run</a>, le système va suprimmer l'ancien container et en créer un nouveau.
</p>

##### --rm

<p style='text-align: justify'>
Automatically remove the container when it exits
</p>

``` shell
docker run --rm $nom_image
```
<div id="IG"></div>

###  Interface Graphique
<p style='text-align: justify'>
Afin de pouvoir afficher un interface graphique à l'écran, nous devons spécifier au container où doit-il afficher l'interface. Pour cela on doit modifier la variable d'environnement DISPLAY. Il faut également un système de fenêtrage X comme <a href="https://fr.wikipedia.org/wiki/Xming">Xming</a>.
</p>

#### Windows

<p style='text-align: justify'>
Installer XLaunch
<br>
<br>
Lancer grâce à XLaunch un Xming Server
</p>

``` shell
docker run -e DISPLAY=YOUR_IP:0.0 $nom_image
```

#### Linux

<div style='color: orange'>Work in progress</div>


 <div id="DS"></div>

###  Diffuser du son

<div style='color: orange'>Work in progress</div>

---
### Documentation des commandes utilisés

<a href="https://docs.docker.com/engine/reference/commandline/run/">Run</a>

---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>

---
###### Sylvain PRAT
