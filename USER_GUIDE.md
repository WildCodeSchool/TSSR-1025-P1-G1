# Guide d'Utilisation - Administration à Distance

## Introduction

Ce guide décrit l'utilisation des outils d'administration à distance 
depuis les postes clients (Windows 11 et Ubuntu 24.04).

**Prérequis** : Les logiciels doivent être installés (voir INSTALL.md)  

---

## Table des Matières

1. [Client Windows 11](#1-client-windows-11)
   - [1.1 Utilisation de base de PuTTY](#11-utilisation-de-base-de-putty)
   - [1.2 Utilisation avancée de PuTTY](#12-utilisation-avancée-de-putty)
   - [1.3 Utilisation de base de TightVNC Viewer](#13-utilisation-de-base-de-tightvnc-viewer)
   - [1.4 Utilisation avancée de TightVNC Viewer](#14-utilisation-avancée-de-tightvnc-viewer)
   - [1.5 Utilisation du Bureau à distance (RDP)](#15-utilisation-du-bureau-à-distance-rdp)
2. [Client Ubuntu 24.04](#2-client-ubuntu-2404)

---
---  

## 1. Client Windows 11

### 1.1 Utilisation de base de PuTTY

#### 1.1.1 Se connecter à un serveur SSH  

**Étape 1:**
 - Entrer une adresse IP dans la case **Host Name (or IP address)**
 - Cliquer sur **Open**
 - Un message d'avertissement apparait
 - Cliquer sur **Accept** pour garder la clé en cache si vous souhaitez vous connecter plus tard sinon sur **Connect Once**

![Sceenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/01_basic_use/01_putty_basic_utilisation.png)    

**Étape 2:**
- Entrer l'identifiant utilisateur de la machine distante
- Entrer le mot de passe de l'utilisateur précédemment entré

![Screenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/01_basic_use/02_putty_basic_utilisation.png)  

**Étape 3:**
- Vous êtes connecté!  

![Sceenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/01_basic_use/03_putty_basic_utilisation.png)    

---
---

### 1.2 Utilisation avancée de PuTTY

#### 1.2.1 Sauvegarder les connexions distantes

- Entrer l'adresse IP du poste distant dans **Host Name (or IP address)**
- Entrer un nom de session dans **Saved Sessions**
- Cliquer sur **Save**
- Sélectionner la session sauvegardée
- Cliquer sur **Open** pour ouvrir la connexion

![Sceenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/02_advanced_use/01_putty_save/01_putty_save.png)  

#### 1.2.2 Personnaliser l'apparence

**Étape 1:**  
- Sélectionner la session à personnaliser
- Cliquer sur **Load** pour charger le profil de session
- Une adresse IP devrait apparaître si elle a été saisie lors de la sauvegarde de la session
- Cliquer sur **Appearance** 
- Cliquer sur **Change** pour changer la police d'écriture

![Sceenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/02_advanced_use/02_putty_appearence/01_putty_appearance.png)   

**Étape 2:**  
- Choisir une **Police**, un **Style de police** et une **Taille**
- Cliquer sur **OK**
- Les changements apparaissent dans l'interface de **Appearance**

![Sceenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/02_advanced_use/02_putty_appearence/02_putty_appearance.png)   

**Étape 3:**  
- Cliquer sur **Colours**
- Sélectionner un élément parmi :
   - **Default Foreground** => Texte par défaut
   - **Default Bold Foreground** => Texte gras par défaut
   - **Default Background** => Fond par défaut
   - **Default Bold Background** => Fond du texte gras
- Cliquer sur **Modify**
- Sélectionner une couleur pour changer la valeur de l'élément sélectionné
- Cliquer sur **OK** pour valider

![Sceenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/02_advanced_use/02_putty_appearence/03_putty_appearance.png) 

**Étape 4:**  

- Dès que les modifications sont terminées
- Cliquer sur **Session**
- Sélectionner la session à modifier
- Cliquer sur **Save**
- Cliquer sur **Open** pour vérifier vos modifications

![Sceenshot - Utilisation PuTTY](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/PuTTY/02_advanced_use/02_putty_appearence/04_putty_appearance.png) 

---  
---  

### 1.3 Utilisation de base de TightVNC Viewer

#### 1.3.1 Se connecter à un serveur VNC  

**Étape 1:**

- Cliquer deux fois sur l'icône de TightVNC Viewer
- Entrer une adresse IP dans **Remote Host**
- Cliquer sur **Connect**
- Entrer le mot de passe configuré sur VNC Server sur le poste distant dans **Password**

![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/VNC/01_basic_use/01_vnc_basic_utilisation.png) 

**Étape 2:**
- Vous êtes connecté!  
  
![Sceenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/VNC/01_basic_use/02_vnc_basic_utilisation.png)   

---  
---

### 1.4 Utilisation avancée de TightVNC Viewer

#### 1.4.1 Sauvegarde d'une session TightVNC  

**Étape 1:**

- Cliquer sur l'icône de disquette pour sauvegarder la session TightVNC
- Choisir un nom de fichier
- Enregistrer la session

![Screenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/VNC/02_advanced_use/01_save_remote/01_vnc_advanced_utilisation_save_remote.png)

**Étape 2:**

- Si vous souhaitez vous connecter à la session sans entrer de mot de passe, cliquer sur **oui**
- Cliquer deux fois sur l'icône qui apparaît à l'endroit où le fichier a été sauvegardé pour ouvrir la session

![Screenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/VNC/02_advanced_use/01_save_remote/02_vnc_advanced_utilisation_save_remote.png)  

---  

#### 1.4.2 Transfert de fichier (Démonstration avec la création d'un dossier) 

**Étape 1:**

- Dans TightVNC, cliquer sur l'icône de double fichier dans la barre d'outils
- Création d'un dossier sur l'ordinateur Hôte en cliquant sur mkdir

![Screenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/VNC/02_advanced_use/02_files_transfer/01_vnc_advanced_utilisation_file_transfer.png)

**Étape 2:**  

- Dans la fenêtre qui apparaît, créer un nom de dossier
- Sélectionner le dossier créé
- Cliquer sur les doubles flèches pour initialiser le transfert du dossier sur le poste distant
- Valider le transfert du dossier

![Screenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/VNC/02_advanced_use/02_files_transfer/02_vnc_advanced_utilisation_file_transfer.png)

**Étape 3:**  

- Le dossier a bien été transféré sur l'interface de TightVNC
- Le dossier est bien présent dans l'explorateur de la machine

![Screenshot - TightVNC](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/VNC/02_advanced_use/02_files_transfer/03_vnc_advanced_utilisation_file_transfer.png)

---
---

### 1.5 Utilisation du Bureau à distance (RDP)

#### 1.5.1 Se connecter à Windows Server

**Étape 1:**
- Cliquer sur le menu **Démarrer**
- Taper dans la barre de recherche **RDP**
- Sélectionner **Connexion Bureau à distance**
- L'application s'affiche
- Entrer l'adresse IP de la machine distante

![Screenshot - RDP](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/RDP/01_basic_use/01_rdp_basic_utilisation.png)  

**Étape 2:** 
- Entrer le nom d'utilisateur et le mot de passe de la machine distante
- Cocher **Mémoriser mes informations** si vous souhaitez garder les informations de connexion
- Cliquer sur **OK**
- Cliquer sur **Oui** pour accepter le certificat et se connecter  

![Screenshot - RDP](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/RDP/01_basic_use/02_rdp_basic_utilisation.png)  

**Étape 3:** 
- Vous êtes connecté!

![Screenshot - RDP](https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Screens_USER_GUIDE/Client_Windows/RDP/01_basic_use/03_rdp_basic_utilisation.png)  

---
---

## 2. Client Ubuntu 24.04

### 2.1 Utilisation de base de TightVNC

- Allumer votre machine client Linux Ubuntu, ici appelée "ubu01", et en parallèle votre machine serveur Windows, ici appelée "srvwin01".



---

- Rendez-vous dans le Terminal d'Ubuntu et taper ensuite la ligne de commande `vncviewer srvwin01` pour ouvrir le logiciel TightVNCViewer sur votre serveur (`srvwin01` étant le nom attribué à la machine serveur sur votre machine client mais vous auriez pu bien évidemment mettre l'adresse IP du serveur à la place).

- Taper le mot de passe choisi au préalable sur le serveur VNC sur la machine serveur Windows.

![Image01]()

---

- Une fenêtre se lance : "TightVNC : srvwin01".

- Regarder simultanément les écrans de "ubu01" et "srvwin01".

![Image02]()   


### Vous voilà connecté !

---
Bonus : Pour vous déconnecter de "srvwin01", il vous suffit d'appuyer sur la croix de la fenêtre lancée.   

---
---

### 2.2. Utilisation de Base d'OpenSSH

- Allumer votre machine client Linux Ubuntu, ici appelée "ubu01", et en parallèle votre machine serveur Linux Debian, ici appelée "srvlx01", en vous connectant sur votre compte utilisateur.

- Rendez-vous dans le Terminal d'Ubuntu et taper ensuite la ligne de commande ssh suivante  
`nom_utilisateur@adresse_ip_ou_nom_du_serveur` (ici wilder@srvlx01) pour ouvrir la suite logicielle OpenSSH sur votre serveur (`srvlx01` étant le nom attribué à la machine serveur sur votre machine client mais vous auriez pu bien évidemment mettre l'adresse IP du serveur à la place).  
Normalement, vous n'avez pas besoin d'entre le mot de passe du serveur car vous avez préalablement générer un clé SSH conformément aux instructions du fichier INSTALL.



### Vous voilà connecté !

---

- Pour vous déconnecter, il vous suffit simplement de taper la ligne de commande `logout` dans le Terminal.



---
---

2.3. Utilisation avancée d'OpenSSH  

Nous allons maintenant voir comment transférer un fichier d'une machine Client Linux Ubuntu, ici, appelée "ubu01" à une machine Serveur Linux Debian, ici appelée "srvlx01". Et comment en récupérer un du serveur Linux ("srvlx01") au client Linux ("ubu01") depuis le Terminal du client Linux ("ubu01").

---
- Mettez en route vos deux machines Linux simultanément (Client et Serveur).



