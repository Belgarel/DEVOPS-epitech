# Projet DEVOPS (Network & Sysadmin - T-NSA-700) - Epitech MsC 1
Umbrella project for T-NSA-700 (school project)

## Participants

* BRIERE Nicolas
* MALAISE Arthur
* MARCHAND Laura
* MAMMAR Said

## Environnement

### [TODO] Créer la première VM (gitlab)

* Téléchargez [packer](https://www.packer.io/downloads.html)
* Placez-vous dans le dépôt et lancez la commande : [votre/chemin/vers/packer] build packer/devopsgitlab.json

### La VM de base (gitlab)

Téléchargez la machine [devopsgitlab](https://epitechfr-my.sharepoint.com/:u:/r/personal/adrien_marchand_epitech_eu/Documents/devopsgitlab.zip?csf=1&e=nCbgOg) à partir de laquelle vous créerez les autres machines.

Utilisateurs par défaut :
* root/dev0ps
* devops/dev0ps

### VMs à créer

Pour traiter le sujet, les environnements suivants sont nécessaires :

Nom de machine    | hostname | utilisateur     | mot de passe
----------------- | -------- | --------------- | ----------------
devopsgitlab      | gitlab   | gitlab          | g1tlab
devopsansible     | ansible  | ansible         | ansibl3
devopsansible     | ansible  | dev             | d3v
devopspfront      | pfront   | front           | fr0nt
devopspapp        | papp     | app             | App
devopspbdd        | pbdd     | bdd             | Bdd

### Procédure pour copier une VM

Réalisez une copie du dossier la machine **devopsgitlab** et renommez-le en **devopscible**
* Changez les noms des fichiers en **devopscible**
* Faites un rechercher-remplacer **devopsgitlab** => **devopscible** dans les fichiers suivants :
 * vmware.log
 * vmware-0.log
 * vmware-1.log
 * devopscible.vmx
 * devopscible.vmxf
 * devopscible.vmdk
* Avec VMware, ouvrez votre VM et démarrez-la
* Créez votre utilisateur avec la commande `useradd -m [utilisateur]` et entrez le mot de passe avec `passwd [utilisateur]`
* Changez le nom du serveur dans le fichier : `/etc/hostname`
* Arrêtez la machine `shutdown now`
* **Avant de démarrer**, allez dans VMWare (clic droit) > `Settings` > `Network Adapter`
  * sélectionnez `Bridged` pour toutes les machines
  * dans `Advanced` cliquez sur `Generate` pour créer une nouvelle nouvelle adresse MAC
* Sur chaque machine, `apt-get install openssh-server`. Faites `ip a` pour connaître l'adresse ip de la machine
* Sur chaque machine (en particulier ansible), modifiez `/etc/hosts` de façon à pouvoir accéder aux autres machines avec la commande `ssh [utilisateur]@[hostname]`. Depuis ansible :
  * `ssh app@app`
  * `ssh bdd@bdd`
  * `ssh front@front`
  * `ssh gitlab@gitlab`

**Remarque :** sur la machine template, il reste nécessaire de créer l'utilisateur `gitlab`

## Dépôts Gitlab

Une fois que vous avez créé vos VMs, placez-vous à l'intérieur, clonez vos dépôts, et commencez à travailler :)

* Projet [gitlab](https://github.com/Belgarel/DEVOPS-epitech-gitlab)
* Projet [ansible](https://github.com/Belgarel/DEVOPS-epitech-ansible)
