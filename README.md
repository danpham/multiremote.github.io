Project MutliRemote
=============================

# Pages
- [Installation d'une mise à jour](#installation)
- [Installation d'une mise à jour](#Link)

----------------------------------

# Installation


## Paquetage


## MultiRemote LCD
dsfdsf
dsfs
fs
f
sdfs
dsfdsf
dsfs
fs
f
sdfs
dsfdsf
dsfs
fs
f
sdfs
## MultiRemote STM32

dsfdsf
dsfs
fs
f
sdfs
# MultiRemote ESP32
## Matériel
- Adaptateur USB To Uart 5V/3V3
- Câble USB-A vers USB-micro

## Installation
- Positionner le micro-switch de Adaptateur USB To Uart 5V/3V3 sur 3V3.
- Connecter le câble USB-A vers USB-micro au PC et sur l'adaptateur.
  
## Logiciel
### Installation
Télécharger et installer Python:
https://www.python.org/ftp/python/3.12.0/python-3.12.0-amd64.exe

Sur Windows, ouvrir une ligne de commande puis taper :
```
pip install esptool
```

### Mise à jour
Rechercher le port de la liaison série de l'Adaptateur USB To Uart.
Sur Windows, aller dans Gestionnaire de périphériques puis identifier le port COMx du périphériques USB-SERIAL CH340.

![image](https://github.com/danpham/multiremote.github.io/assets/150057/b8b4b2e0-54bc-4c9d-9046-6af552cdf695)

Sur Windows, ouvrir une ligne de commande puis taper :
```
esptool.py --baud 115200 --port COMx write_flash 0x0 multiremote_esp32_v1_0_0.bin
```
