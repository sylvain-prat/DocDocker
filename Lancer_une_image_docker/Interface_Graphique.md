<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

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


---
### Documentation des commandes utilisés

<a href="https://docs.docker.com/engine/reference/commandline/run/">Run</a>

---

###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/Lancer_une_image_docker/lancement_image_docker.md">Lancement image Docker</a>

---
###### Sylvain PRAT
