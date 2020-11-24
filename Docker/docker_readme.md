# Installation de Docker

Source : https://ios.dz/installation-docker-ce-centos-8/

```
cd /tmp
wget -P /tmp/ https://download.docker.com/linux/centos/7/x86_64/stable/Packages/containerd.io-1.2.13-3.1.el7.x86_64.rpm
sudo dnf localinstall /tmp/containerd.io-1.2.13-3.1.el7.x86_64.rpm -y
```
```` 
# Mise à jour du cache  
dnf makecache 
# installation des dépendances nécessaires"  
sudo dnf install dnf-utils wget vim nano device-mapper-persistent-data lvm2 fuse-overlayfs -y 
# ajout du repository officiel Docker"  
sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
````

````
# Mise à jour du cache"  
dnf makecache 
# installation de docker-ce"  
sudo dnf install docker-ce -y 
# start & enable du service docker"  
sudo systemctl enable --now docker 
# Docker est installé avec succès, vérification de la version :"  
docker --version 
#On vérifie que Docker tourne
systectl status docker
````