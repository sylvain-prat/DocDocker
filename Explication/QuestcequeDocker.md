<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

<img  src="https://d1.awsstatic.com/acs/characters/Logos/Docker-Logo_Horizontel_279x131.b8a5c41e56b77706656d61080f6a0217a3ba356d.png" />

##### Docker c'est quoi ?

<p style='text-align: justify'>
Docker est un logiciel libre qui permet d'encapsuler une application et ses dépendances dans un container. Contrairement à une virtualisation, la conteneurisation est beaucoup plus  léger car il utilise certaine partie de la machine hôte, notamment le système d'exploitation. Docker est donc un excellent moyen de rendre ses applications cross plateform et de faciliter le déploiment de celle ci.
</p>

##### Un container ?

<p style='text-align: justify'>
Un container fonctionne de façon isolé mais s'appuie sur des fonctionnalité de la machine comme le système d'exploitation, utilise l'isolation de ressource ainsi que des espaces de noms séparés pour isoler le système tel que vu par l'application. Tout container est basé sur un système d'exploitation. Il existe donc plusieurs types de container comme par exemple les container linux ou windows. Pour fonctionner, les containers ont besoin de l'OS qui leur est associé pour fonctionner. Par exemple un container windows a besoin d'être lancé depuis un environement windows.
</p>

##### Pourquoi Docker se vend comme un logiciel permettant un cross plateform si chaque container a besoin de l'os qui lui est associé ?

<p style='text-align: justify'>
Tous les containers ne sont pas utilisable sur tous les système d'exploitation. Cependant les logiciels Docker, comme Docker for windows, permettent d'utiliser des container linux. Les container linux sont donc les seuls à proposer un réel cross plateform.
</p>


##### Comment ça marche ?

<p style='text-align: justify'>
Le logiciel docker a automatisé la création d'un container. Pour créer un container il est nécessaire d'avoir une image docker. Une image docker est un peu comme un model permettant la création d'un ou plusieurs container. Afin de créer une image il suffit de créer un fichier nommé Dockerfile. Le Dockerfile est un fichier contenant toute les instructions permettant la création d'une image docker.
</p>

##### Est ce que je peux associer plusieurs image docker entre elle ?

<p style='text-align: justify'>
Docker propose un système nommé docker-composer qui permet de faire intéragir des images entre elles.
</p>


---
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>

---
###### Sylvain PRAT
