# Documentation d'Installation - Administration à Distance

## Contexte du Projet
Ce document décrit l'installation et la configuration des outils d'administration à distance dans un environnement réseau local comprenant des machines Windows et Linux.

---

## Table des Matières
1. [Prérequis Techniques](#1-prérequis-techniques)
2. [Installation sur Windows Server 2022](#2-installation-sur-windows-server-2022)
3. [Installation sur Debian 13](#3-installation-sur-debian-13)
4. [Installation sur Windows 11 (Client)](#4-installation-sur-windows-11-client)
   - [4.1 PuTTY](#41-putty)
   - [4.2 TightVNC](#42-tightvnc)
6. [Installation sur Ubuntu 24.04 (Client)](#5-installation-sur-ubuntu-2404-client)
7. [FAQ et Dépannage](#6-faq-et-dépannage)

---

## 1. Prérequis Techniques

### 1.1 Infrastructure Réseau
- **Topologie** : Réseau local privé avec adressage IP statique
- **Configuration requise** :
  - Serveur Windows Server 2022
  - Serveur Debian 13
  - Client Windows 11 Pro
  - Client Ubuntu 24.04
- **Connectivité** : Toutes les machines doivent pouvoir communiquer sur le réseau local

### 1.2 Configuration IP
Assurez-vous que chaque machine possède :
- Une adresse IP statique configurée sur le réseau (172.16.10.0)
- Un masque de sous-réseau 255.255.255.0

### 1.3 Logiciels Nécessaires

#### Pour Windows Server 2022
- TightVNC Server (pour l'accès distant graphique)
- OpenSSH Server (natif Windows Server)

#### Pour Debian 13
- OpenSSH Server (pour les connexions SSH)
- Accès root ou sudo

#### Pour Windows 11 (Client)
- PuTTY (pour SSH vers Debian)
- TightVNC Viewer (pour VNC vers Windows Server)
- Client RDP (natif Windows)

#### Pour Ubuntu 24.04 (Client)
- OpenSSH Client (généralement préinstallé)
- TightVNC Viewer ou Remmina (pour VNC vers Windows Server)

---


## 4. Installation sur Windows 11 (Client)

## 4.1 PuTTY  

### 4.1.1 Téléchargement de PuTTY  

- Télécharger PuTTY depuis le site officiel : https://www.putty.org/
- Lien direct vers la dernière version à installer : https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.83-installer.msi
- Lien direct vers la dernière version portable (passer directement à l'étape 3) : https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe

--- 

### 4.1.2 Installation de PuTTY  

**Étape 1 : Accueil et choix du dossier d'installation**

- Double-cliquer sur le fichier d'installation téléchargé
- L'assistant d'installation **PuTTY** s'affiche
- Cliquer sur **Next**
- Le dossier par défaut proposé est `C:\Program Files\PuTTY\`
- Conserver ce dossier ou cliquer sur **Change** pour le modifier
- Cliquer sur **Next**

![Sceenshot - PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/PuTTY/02_putty_installation.png)  

---

**Étape 2 : Sélection des fonctionnalités et finalisation d'installation**

- Sélectionner les options souhaitées :
   - **Install PuTTY files**
   - **Add shortcut to PuTTY on the Desktop** (pour créer un raccourci bureau, il n'est pas activé par défaut)
   - **Put install directory on the PATH for command prompts**
   - **Associate .PPK files with PuTTYgen and Pageant**
- Cliquer sur **Install**
- L'installation est terminée
- Cocher **View README file** si vous souhaitez consulter la documentation
- Cliquer sur **Finish**
 
![Sceenshot - PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/PuTTY/02_putty_installation.png)

---

**Étape 3 : Première utilisation et connexion** 
- Entrer une adresse IP dans la case **Host Name (or IP address)**
- Cliquer sur **Open**
- Un message d'avertissement apparait
- Cliquer sur **Accept** pour garder la clé en cache si vous souhaitez vous connecter plus tard sinon sur **Connect Once**

![Sceenshot - PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/PuTTY/03_putty_installation.png)

---

**Étape 4 : Login et Password**
- Entrer l'identifiant utilisateur de la machine distante
- Entrer le mot de passe de l'utilisateur précédemment entré

![Sceenshot - PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/PuTTY/04_putty_installation.png)

---

**Étape 5 : Vous êtes connecté!**  

![Sceenshot - PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/PuTTY/05_putty_installation.png)  

---
---  

# 4.2 TightVNC  

### 4.2.1 Téléchargement de TightVNC Viewer

- Télécharger TightVNC depuis le site officiel : https://www.tightvnc.com/
- Lien direct vers la dernière version : https://www.tightvnc.com/download/2.8.85/tightvnc-2.8.85-gpl-setup-64bit.msi

---

### 4.2.2 Installation de TightVNC Viewer

**Étape 1 : Accueil et acceptation des termes de la licence**

- Double-cliquer sur le fichier d'installation
- L'assistant **TightVNC Setup** s'affiche
- Cliquer sur **Next**
- Cocher **I accept the terms in the License Agreement**
- Cliquer sur **Next**

![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/TightVNC/01_vnc_installation.png)

---

**Étape 2 : Choix du type d'installation et choix des composants**

- Sélectionner **Custom** (pour choisir les composants à installer)
- Cliquer sur **Next**
- Dans l'arborescence, **enlever** **TightVNC Server** ( Sur le poste client nous utilisons seulement le viewer)
- Cliquer sur **Next**  

![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/TightVNC/02_vnc_installation.png)  

---

**Étape 3 : Associations des fichiers et installation**

- Sous **File associations**, cocher **Associate .vnc files with TightVNC Viewer**
   - Cette option permet d'ouvrir automatiquement les fichiers `.vnc` avec TightVNC
- Cliquer sur **Next**
- L'écran **Ready to install TightVNC** confirme les paramètres
- Cliquer sur **Install** pour lancer l'installation

![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/TightVNC/03_vnc_installation.png)  

---

**Étape 4 : Fin de l'installation**

- Cliquer sur **Finish**
- Ouvrir le menu Démarrer de Windows 11
- Rechercher **"tight"** dans la barre de recherche
- **TightVNC Viewer** apparaît dans les résultats sous **Meilleur résultat** ( TightVNC ne met pas de raccourci sur le bureau par défaut)
- Cliquer sur **TightVNC Viewer**  

![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/TightVNC/04_vnc_installation.png)  

 ---

**Étape 5 : Première utilisation et connexion**
- Entrer une adresse IP dans **Remote Host**
- Cliquer sur **Connect**
- Entrer le mot de passe configurer sur VNC Server sur le poste distant dans **Password**  

![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/TightVNC/05_vnc_installation.png)  

---  

**Étape 6 : Vous êtes connecté!**    

![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Windows/TightVNC/06_vnc_installation.png)  

---
---

# V. Installation du Client Linux

##  1. Installation du serveur VNC

  Installation d'une application VNC, TightVNCViewer, sur un client Linux, dans le cas présent sur la version d'Ubuntu 24.04 LTS à jour pour le lier à une machine virtuelle serveur Windows et se connecter dessus. Le serveur en question est l'OS Windows Server 2022 GUI (interface graphique), préalablement installé et configuré de TightVNCServer (Voir partie I).   

<br>

---
 
- Mettre en route la machine Ubuntu qui se nomme ici "ubu01".

- Il vous faut ouvrir le Terminal d'Ubuntu. Cliquer sur le logo d'Ubuntu (Dock) en bas à gauche de l'écran ensuite cliquer sur l'icône sous laquelle est écrit Terminal s'il apparaît.

![Image01](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/01_TightVNC_Client_Linux.png)

---
- Sinon rechercher l'application Terminal directement dans la barre de recherche.

- Ouvrir donc le Terminal.

![Image02](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/02_TightVNC_Client_Linux.png)

---
- Entrer la ligne de commande `apt install xtightvncviewer` pour installer le logiciel TightVNCViewer.

- On constate qu'un message d'erreur apparaît concernant les droits utilisateurs.

![Image03](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/03_TightVNC_Client_Linux.png)

---
- On force l'installation en ajoutant la commande `sudo` à la précédente ligne de commande : `sudo apt install xtightvncviewer`

- Ne pas oublier d'ajouter le mot de passe permettant d'accéder aux droits administrateurs.

![Image04](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/04_TightVNC_Client_Linux.png)

---
- Tapez `O` et laissez l'installation s'opérer.

![Image05](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/05_TightVNC_Client_Linux.png)

---
- Une fois l'installation effectuée, mettre en route à côté la machine serveur Windows, ici nommée "srvwin01".

<img src="https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/06_TightVNC_Client_Linux.png" width="500" height="400"/>

---
- Vérifier que le processus TightVNCServer est bien actif :   
  Deux manières de faire :

<br>
  
  a) Avec une invite de commandes ou plus communément appelé "Shell" :

* Rechercher dans la barre de recherche le logiciel "PowerShell".

* Ouvrir PowerShell en tant qu'Administrateur avec une action de clic droit dessus.
  
![Image07](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/07_TightVNC_Client_Linux.png)
   
---
     
* Taper la ligne de commande `Get-Process -Name tvnserver`.

* On constate que le processus "tvnserver" est bien en cours.

![Image08](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/08_TightVNC_Client_Linux.png)
   
---
     
* "tvnserver" étant le processus de TightVNCServer, on peut le vérifier avec la ligne de commande suivante :  
`Get-Process -Name tvnserver -FileVersionInfo | Format-List`

* On constate donc que "tvnserver" est en cours et qu'il s'agit bien du processus de TightVNCServer.

![Image09](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/09_TightVNC_Client_Linux.png)
      
---
  b) Directement sur l'interface graphique :
 
* Cliquer sur la flèche dans la barre des tâches.
* Cliquer sur l'icône V entouré d'un carré blanc.

* On constate bien que TightVNCServer est en cours.
    
![Image10](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/10_TightVNC_Client_Linux.png)
    
---
- Laisser de côté "srvwin01" et revenir sur "ubu01". Taper ensuite la ligne de commande `vncviewer srvwin01` pour ouvrir le logiciel TightVNCViewer.

- Taper le mot de passe choisi au préalable sur le serveur VNC sur la machine serveur Windows.

![Image11](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/11_TightVNC_Client_Linux.png)

---
- Une fenêtre se lance : "TightVNC : srvwin01".

- Regarder simultanément les écrans de "ubu01" et "srvwin01".

![Image12](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/TightVNC/12_TightVNC_Client_Linux.png)
  

### **Voilà, vous avez connecté le client Linux au serveur Windows !**   
---

<br>
<br>
<br>
<br>


## 2. Mise en place du serveur SSH

  Installation de la suite logicielle OpenSSH sur un client Linux, dans le cas présent sur la version d'Ubuntu 24.04 LTS à jour pour le lier à une machine vituelle serveur Linux et se connecter dessus. Le serveur en question est l'OS Debian 13.1.0 CLI (interface d'invite de commandes).  

<br>

---

- Mettre en route la machine Ubuntu qui se nomme ici "ubu01".

- Ouvrir le Terminal. (Se référer au 1. pour le localiser.)

![Image01](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/01_OpenSSH_Client_Linux.png)

---

- Entrer la ligne de commande `apt install openssh-client` pour installer le client OpenSSH.
- On constate qu'un message d'erreur apparaît concernant les droits utilisateurs.

- On force l'installation en ajoutant la commande `sudo` à la précédente ligne de commande : `sudo apt install openssh-client`.

![Image02](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/02_OpenSSH_Client_Linux.png)

---


- Ne pas oublier d'ajouter le mot de passe permettant d'accéder aux droits administrateurs.

- Laisser l'installation s'opérer.

![Image03](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/03_OpenSSH_Client_Linux.png)

---

- Une fois l'installation effectuée, mettre en route à côté la machine serveur Linux (Debian), ici nommée "srvlx01".

- Se connecter en tant qu'administrateur et entrer son mot de passe.

![Image04](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/04_OpenSSH_Client_Linux.png)

---

- Vérifier si l'OS est à jour avec la ligne de commande `apt install update && apt upgrade`. (Ce dernier est à jour dans le cas présent.)

![Image05](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/05_OpenSSH_Client_Linux.png)

---

- Installer le serveur OpenSSH avec la commande `apt install openssh-server`.

![Image06](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/06_OpenSSH_Client_Linux.png)

---

- Vérifier le statut d'OpenSSH avec la commande `systemctl status ssh`.

- S'il n'est pas actif comme indiqué dans les lignes "Loaded" (2x "enabled" en vert) et "Active" ("active (running)" en vert), entrer les commandes à la suite les commandes `systemctl start ssh` et `systemctl enabled ssh` pour activer le service SSH.

![Image07](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/07_OpenSSH_Client_Linux.png)

---
- Laisser de côté "srvlx01" et revenir sur "ubu01".      
Taper ensuite la ligne de commande `ssh nom_utilisateur@adresse_ip_ou_nom_du_serveur`.

Ici le nom d'utilisateur est "wilder" et le nom du serveur est "srvlx01", comme celui de la machine, avec comme adresse ip 172.16.10.6 auparavant indiqué dans les prérequis) pour créer une clé SSH avec la machine "srvlx01".
 
- Taper `yes` et taper ensuite le mot de passe de la machine "srvlx01" (préalablement choisi dans la partie II).

![Image08](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/08_OpenSSH_Client_Linux.png)

---
- On constate bien un changement nom de machine à côté du `@` .

![Image09](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_INSTALL/Client_Linux%20/OpenSSH/09_OpenSSH_Client_Linux.png)

### **Voilà, vous avez connecté le client Linux au serveur Linux !**
 
---
