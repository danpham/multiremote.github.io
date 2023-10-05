Project MutliRemote
=============================

# Pages
- Installation d'une mise à jour

----------------------------------

# Installation


## Paquetage


## MultiRemote LCD

## MultiRemote STM32

# MultiRemote ESP32
## Matériel
- Adaptateur USB To Uart 5V/3V3
- Câble USB-A vers USB-micro

## Installation
- Positionner le micro-switch de Adaptateur USB To Uart 5V/3V3 sur 3V3.
- Connecter le câble USB-A vers USB-micro au PC et sur l'adaptateur.
  
## Logiciel
### Installation
- Télécharger et installer Python:
https://www.python.org/ftp/python/3.12.0/python-3.12.0-amd64.exe

### Mise à jour
- Déterminer le port COMx correspondant à l'adapteur Adaptateur USB To Uart en ouvrant le 'Gestionnaire de périphériques' Windows.
![image](https://github.com/danpham/multiremote.github.io/assets/150057/038936b2-5daa-4afe-b7f6-6eaf2739dc59)

- Sur Windows, ouvrir une ligne de commande puis taper :
```
esptool.py --baud 115200 --port COMx write_flash 0x0 multiremote_esp32_v1_0_0.bin
```
Avec COMx, x est le numéro du port COM 

# MultiRemote STM32
## Matériel
- Sonde STLINK-V3SET
- Câble USB-A vers USB-micro

## Installation

- Connecter le câble USB-A vers USB-micro au PC et sur l'adaptateur.
  
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

