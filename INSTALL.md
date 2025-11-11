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

![Sceenshot - PuTTY](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/PuTTY/01_putty_installation.png)  

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
 
![Sceenshot - PuTTY](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/PuTTY/02_putty_installation.png)

---

**Étape 3 : Première utilisation et connexion** 
- Entrer une adresse IP dans la case **Host Name (or IP address)**
- Cliquer sur **Open**
- Un message d'avertissement apparait
- Cliquer sur **Accept** pour garder la clé en cache si vous souhaitez vous connecter plus tard sinon sur **Connect Once**

![Sceenshot - PuTTY](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/PuTTY/03_putty_installation.png)

---

**Étape 4 : Login et Password**
- Entrer l'identifiant utilisateur de la machine distante
- Entrer le mot de passe de l'utilisateur précédemment entré

![Sceenshot - PuTTY](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/PuTTY/04_putty_installation.png)

---

**Étape 5 : Vous êtes connecté!**  

![Sceenshot - PuTTY](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/PuTTY/05_putty_installation.png)  

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

![Sceenshot - TightVNC](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/TightVNC/01_vnc_installation.png)

---

**Étape 2 : Choix du type d'installation et choix des composants**

- Sélectionner **Custom** (pour choisir les composants à installer)
- Cliquer sur **Next**
- Dans l'arborescence, **enlever** **TightVNC Server** ( Sur le poste client nous utilisons seulement le viewer)
- Cliquer sur **Next**  

![Sceenshot - TightVNC](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/TightVNC/02_vnc_installation.png)  

---

**Étape 3 : Associations des fichiers et installation**

- Sous **File associations**, cocher **Associate .vnc files with TightVNC Viewer**
   - Cette option permet d'ouvrir automatiquement les fichiers `.vnc` avec TightVNC
- Cliquer sur **Next**
- L'écran **Ready to install TightVNC** confirme les paramètres
- Cliquer sur **Install** pour lancer l'installation

![Sceenshot - TightVNC](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/TightVNC/03_vnc_installation.png)  

---

**Étape 4 : Fin de l'installation**

- Cliquer sur **Finish**
- Ouvrir le menu Démarrer de Windows 11
- Rechercher **"tight"** dans la barre de recherche
- **TightVNC Viewer** apparaît dans les résultats sous **Meilleur résultat** ( TightVNC ne met pas de raccourci sur le bureau par défaut)
- Cliquer sur **TightVNC Viewer**  

![Sceenshot - TightVNC](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/TightVNC/04_vnc_installation.png)  

 ---

**Étape 5 : Première utilisation et connexion**
- Entrer une adresse IP dans **Remote Host**
- Cliquer sur **Connect**
- Entrer le mot de passe configurer sur VNC Server sur le poste distant dans **Password**  

![Sceenshot - TightVNC](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/TightVNC/05_vnc_installation.png)  

---  

**Étape 6 : Vous êtes connecté!**    

![Sceenshot - TightVNC](https://github.com/christianwildcodeschool-dotcom/firstscripting/blob/main/TightVNC/06_vnc_installation.png)  

---
