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
* Créez votre utilisateur avec la commande `useradd [utilisateur] -p` (entrez ensuite le mot de passe)
* Changez le nom du serveur dans le fichier : `/etc/hostname`

**Remarque :** sur la machine template, il reste nécessaire de créer l'utilisateur `gitlab`

## Dépôts Gitlab

Une fois que vous avez créé vos VMs, placez-vous à l'intérieur, clonez vos dépôts, et commencez à travailler :)

* Projet [gitlab](https://github.com/Belgarel/DEVOPS-epitech-gitlab)
* Projet [ansible](https://github.com/Belgarel/DEVOPS-epitech-ansible)
