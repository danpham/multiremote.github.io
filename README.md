Project MutliRemote
=============================

# Pages
- Installation d'une mise à jour

----------------------------------

# Installation


## Paquetage

- Le paquetage MultiRemote est composé de 3 logiciels, chacun étant destiné à un microcontrôleur présent sur la carte.
Le paquetage est distribué sous forme de fichier .zip de mise à jour avec le nom type suivant: update_multiremote_vXX_YY_ZZ

XX correspond au numéro de version majeur, YY correspond au numéro de version mineur et ZZ au correctif.

Les fichiers de mise à jour adoptent également le même formatage du numéro de version mais ces derniers peuvent avoir une version différente.

- multiremote_lcd_vXX_YY_ZZ.bin
- multiremote_stm32_vAA_BB_CC.bin
- multiremote_esp32_vDD_EE_FF.bin

## Compatibilité

Au sein d'un même paquetage, la compatibilité entre les 3 logiciels est garantie et il faudra de fait réaliser les 3 mises à jour à la fois. 

## MultiRemote LCD
## Matériel
- Sonde IAR Systems I-Jet - [Lien constructeur](https://www.iar.com/ijet)

 <img src="https://github.com/danpham/multiremote.github.io/assets/150057/2bcfe4c3-3da6-427e-b7b0-c590c5b72949" height="150"> 

- Câble USB-A vers USB-micro

## Installation

- Connecter le câble USB-A vers USB-micro au PC et sur la sonde I-Jet.
- Connecter le connecteur de la sonde I-Jet sur le carte de l'écran LCD comme sur la photo suivante :

 <img src="https://github.com/danpham/multiremote.github.io/assets/150057/22f12152-891c-4359-b589-a979c196d681" height="250">

## Logiciel
### Installation
- Installer le logiciel IAR Embedded Workbench for ARM 8.40.1 en cliquant sur EWARM-CD-8401-21539.exe.
- Installer GitHub Desktop : https://desktop.github.com
- Télécharger les sources du projet ESP32 avec GitHub Desktop : https://github.com/VNSA-SA/MultiRemoteEsp32/

### Mise à jour

- Dans IAR Embedded Workbench, cliquer dans File > Open workspace et charger le fichier workspace.eww :

![image](https://github.com/danpham/multiremote.github.io/assets/150057/03e2711e-892d-447b-b036-77f98dd7c4e9)

- Cliquer sur download and debug (Ctrl + D) pour charger le logiciel.

- Redémarrer la carte pour terminer la mise à jour.

# MultiRemote ESP32
## Matériel
- Adaptateur USB To Uart 5V/3V3 - [Lien constructeur](https://www.seeedstudio.com/USB-To-Uart-5V-3V3-p-1832.html)



- Câble USB-A vers USB-micro

## Installation

- Positionner le micro-switch de Adaptateur USB To Uart 5V/3V3 sur 3V3.
- Connecter le câble USB-A vers USB-micro au PC et sur l'adaptateur.
- Positionner l'Adaptateur USB To Uart 5V/3V3 comme sur la photo suivante :

 <img src="https://github.com/danpham/multiremote.github.io/assets/150057/b62c87e7-b583-4d56-9f39-a2bd80fe5a8e" height="250">

## Logiciel
### Installation
- Télécharger et installer Python :

https://www.python.org/ftp/python/3.12.0/python-3.12.0-amd64.exe

- Ouvrir la ligne de commande Windows et installer esptool :

```
pip install esptool
```

### Mise à jour
- Déterminer le port COMx correspondant à l'adapteur Adaptateur USB To Uart en ouvrant le 'Gestionnaire de périphériques' Windows.

![image](https://github.com/danpham/multiremote.github.io/assets/150057/038936b2-5daa-4afe-b7f6-6eaf2739dc59)

- Ouvrir une ligne de commande puis taper :

```
esptool.py --baud 115200 --port COMx write_flash 0x0 multiremote_esp32_v1_0_0.bin
```
Avec COMx, x est le numéro du port COM

- Redémarrer la carte pour terminer la mise à jour.

# MultiRemote STM32
## Matériel
- Sonde STLINK-V3SET
- Câble USB-A vers USB-micro

## Installation

- Connecter le câble USB-A vers USB-micro au PC et sur l'adaptateur.
- Positionner le connecteur de la sonde STLINK comme sur la photo suivante :

 <img src="https://github.com/danpham/multiremote.github.io/assets/150057/8e5292db-180a-4110-b609-2cc6d314c2c8" height="250">
  
## Logiciel
### Installation
- Télécharger et installer STM32CubeProgrammer software for Win64 (STM32CubePrg-W64) :
https://www.st.com/en/development-tools/stm32cubeprog.html#get-software

### Mise à jour
- Ouvrir STM32CubeProgrammer et cliquer sur '+' puis Open file, selectionez le fichier 'ESP32_MR.bin' :

![image](https://github.com/danpham/multiremote.github.io/assets/150057/81b6a269-3c49-45da-b97a-1f2f2f7a5482)

- Cliquer sur 'Download' :

![image](https://github.com/danpham/multiremote.github.io/assets/150057/50e1a85b-c25f-4a17-ae54-6b273bafdf93)

- Redémarrer la carte pour terminer la mise à jour.

