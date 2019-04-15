<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />  
5 Avenue Pasteur, 13100 Aix-en-Provence

---

# Créer une image docker d'un fichier.py
### 0 - Programme python à notre disposition

main.py

``` python
print("Hello World !")
```

### 1 - Mise en place du Dockerfile
#### 1.1 - Création du fichier Dockerfile

#### 1.2 - Ajout d'une image déjà existante

<p style='text-align: justify'>
Pour fonctionner notre programme nécessite la version 2.7 de python. Sur <a href="https://hub.docker.com/">DockerHub</a> <a href ="https://hub.docker.com/_/python">python</a> nous propose des images pré-construite pour nous faciliter la tâche. Pour ce programme j'ai choisi l'image python:2.7-slim car c'est la version de python qu'il nous faut et il est en version slim donc moins lourd.
</p>

Dockerfile:

``` Dockerfile
FROM python:2.7-slim
```

#### 1.3 - Installation de package suplémentaire
<p style='text-align: justify'>
Notre programme étant très simple, il n'a besoin d'aucun package suplémentaire pour fonctionner.
</p>


#### 1.4 - Ajout des fichiers du programme dans le container
<p style='text-align: justify'>
Nous devons maintenant  ajouter tous les fichiers qui sont nécessaires au fonctionnement de notre programme. Dans notre cas nous n'avons besoin que de main.py que nous placerons à la racine du container.
</p>

Dockerfile:

``` Dockerfile
FROM python:2.7-slim
ADD main.py /
```

#### 1.5 - Ajout de CMD
<p style='text-align: justify'>
Nous devons maintenant indiquer à notre Dockerfile que faire lorsqu'il sera exécuté. Dans notre cas nous souhaitons exécuter :
</p>

``` shell
python /main.py
```

Dockerfile:

``` Dockerfile
FROM python:2.7-slim
ADD main.py /
CMD [ "python", "/main.py" ]
```

### 2 - Création de l'image Docker à partir du Dockerfile
Le répertoire courant est celui contenant le Dockerfile.


``` shell
docker build -t imageprintpython .
```

  Avec cette commande on crée une image docker se nommant imageprintpython à partir du Dockerfile créé précédemment.

On peut vérifier qu'il a bien été créé grâce à cette commande :


``` shell
docker images
```

### 3 - Exécution de notre image

``` shell
docker run imageprintpython
```




---
### Documentation des commandes utilisés

<a href="https://docs.docker.com/engine/reference/commandline/images/">Images</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/build/">Build</a><br>
<a href="https://docs.docker.com/engine/reference/commandline/run/">Run</a>


---
###### Sylvain PRAT
