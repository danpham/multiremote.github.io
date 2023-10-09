# Release note

# Pages
- Description du paquetage de mise à jour
- Historique de version

----------------------------------
## Paquetage de mise à jour
### Description
- Le paquetage MultiRemote est composé de 3 logiciels, chacun étant destiné à un microcontrôleur présent sur la carte.
Le paquetage est distribué sous forme de fichier .zip de mise à jour avec le nom type suivant: update_multiremote_vXX_YY_ZZ

XX correspond au numéro de version majeur, YY correspond au numéro de version mineur et ZZ au correctif.

Les fichiers de mise à jour adoptent également le même formatage du numéro de version mais ces derniers peuvent avoir une version différente.

- multiremote_lcd_vAA_BB_CC.out
- multiremote_stm32_vDD_EE_FF.bin
- multiremote_esp32_vGG_HH_II.bin

### Compatibilité

Au sein d'un même paquetage, la compatibilité entre les 3 logiciels est garantie et il faudra de fait réaliser les 3 mises à jour à la fois.

# Historique de version
## Des paquetages

## ESP32

## STM32

## LCD
v01.01.00:
- Mode Continu ajouté pour le nombrage du carrousel.
- Enregistrement et lecture des temps de setup opérateur sur la carte SD corrigé.
- Affichage de la date et l'heure avec les secondes.
- Gestion de l'heure d'été / heure d'hiver.
