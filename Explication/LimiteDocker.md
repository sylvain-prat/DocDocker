<img style="height: 60px;" src="http://www.lpl-aix.fr/wp-content/uploads/2018/04/LPL_240_180.jpg" />
5 Avenue Pasteur, 13100 Aix-en-Provence

***

# Les Limites de Docker

<p style='text-align: justify'>
Actuellement afin de créer une image docker Windows, il est nécessaire de partir de l'image Windows Server Core ou Nano Server. Ces images ne sont pas compatible avec les versions antérieures à Windows 10 (<a href="https://docs.microsoft.com/en-us/virtualization/windowscontainers/deploy-containers/version-compatibility">Compatibilité Windows Server Core</a>).
Il n'est doc pas possible de dockeriser des applications fonctionnant sur des vieilles versions de Windows. Pour pouvoir rendre facilement utilisable ces vieilles applications, il suffit de télécharger une VM, la configurer puis l'exporter pour que d'autres utilisateurs puissent l'utiliser. Il existe plusieur logiciel afin de réaliser des VM comme par exemple <a href="https://www.virtualbox.org/">VirtualBox</a>.
</p>

---
###### <a href="https://github.com/sylvain-prat/DocDocker/blob/master/README.md">Sommaire</a>

---
###### Sylvain PRAT
