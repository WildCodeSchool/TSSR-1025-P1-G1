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
- OpenSSH Server (natif dans Windows Server)

#### Pour Debian 13
- OpenSSH Server

#### Pour Windows 11 (Client)
- PuTTY (pour SSH vers Debian)
- TightVNC Viewer (pour VNC vers Windows Server)
- Client RDP (natif Windows)

#### Pour Ubuntu 24.04 (Client)
- OpenSSH Client (généralement préinstallé)
- TightVNC Viewer ou Remmina (pour VNC vers Windows Server)

---
