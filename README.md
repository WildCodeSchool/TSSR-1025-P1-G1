# 🖥️ Projet 1 : Téléassistance

<br>

<img src="https://github.com/WildCodeSchool/TSSR-1025-P1-G1/blob/main/Ressources/Image_Teleassistance.png" align="center" width="500" height="500"/>

## Sommaire 

- [🎯 Présentation du projet](#presentation-du-projet)
- [📜 Introduction](#introduction)
- [👥 Membres du groupe par sprint](#membres-du-groupe-par-sprint)
- [⚙️ Choix Techniques](#choix-techniques)
- [🧗Difficultés rencontrées](#difficultes-rencontrees)
- [💡 Solutions trouvées](#solutions-trouvees)
- [🚀 Améliorations possibles](#ameliorations-possibles)

# 🎯 Présentation du projet
<span id="presentation-du-projet"></span>
### La téléassistance

**Présentation**  
Le but de ce projet est la mise en place de systèmes de téléassistance pour la prise de contrôle à distance. Pour cela nous avons utilisés 4 machines en réseaux local et installé plusieurs logiciels pour la communication entre les machines.

**Objectifs finaux**  
Les objectifs finaux de ce projet sont :
 - 1 : la prise de contrôle à distance du : 
      - Client Windows vers Windows Server avec **VNC** et **RDP**
      - Client Windows vers Debian Server avec **PuTTY**
      - Client Linux Vers Windows Server avec **VNC**
      - Client Linux vers Debian Server avec **openssh**

 - 2 : La création d'un groupe local "Assistance" sur le client Windows pour la prise de contrôle à distance
 - 3 : La sécurisation d'une connexion SSH 

# 📜 Introduction
<span id="introduction"></span>

# 👥 Membres du groupe par sprint
<span id="membres-du-groupe-par-sprint"></span>
**Sprint 1**

| Membre     | Rôle       | Missions |
| ---------- | ---------- | -------- |
| Christian  | SM         | Mise en place des serveurs, documentation des serveurs      |
| Sami       | PO         | Mise en place Windows Client, documentation Windows Client  |
| Anis       | Technicien | Mise en place de Linux Client, documentation Linux Client   | 


**Sprint 2**

| Membre     | Rôle       | Missions |
| ---------- | ---------- | -------- |
| Sami       | SM         | - Documentation de Linux Client sur USER_GUIDE.md & INSTALL.md |
| Anis       | PO         | - Documentation des Serveurs (Windows & Linux) sur USER_GUIDE.md & INSTALL.md |
| Christian  | Technicien | - Documentation de Windows Client sur USER_GUIDE.md & INSTALL.md |

# ⚙️ Choix techniques
<span id="choix-techniques"></span>
**Matériel**
- Une machine virtuel avec le système d'exploitation Windows Server 2022
- Une machine virtuel avec le système d'exploitation Debian 13.1 CLI (en interface de ligne de commande)
- Une machine virtuel avec le système d'exploitation Windows 10/11
- Une machine virtuel avec le système d'exploitation Ubuntu LTS 24.04

**Logiciels**
- TightVNCServer pour la machine serveur Windows
- OpenSSHServer (suite logicielle -> déjà intégrée à l'OS) pour la machine serveur Linux
- TightVNCViewer pour la machine client Windows
- PuTTY pour la machine client Windows
- TightVNCViewer pour la machine client Ubuntu
- OpenSSHClient pour la machine client Ubuntu

# 🧗 Difficultés rencontrées
<span id="difficultes-rencontrees"></span>

# 💡 Solutions trouvées
<span id="solutions-trouvees"></span>

# 🚀 Améliorations possibles
<span id="ameliorations-possibles"></span>
