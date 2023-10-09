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
v01.01.00:
 - Prise en compte du mode setup opérateur même si le MultiRemote vient de redémarrer.
 - Correction de la fuite mémoire sur le serveur opcua, lorsqu'une connection se termine anormalement ou que le câble réseau est débranché.
 - Affichage de l'heure de démarrage correcte dans les données du serveur opcua.
   
## STM32
v01.01.00:
 - Ajout du mode échantillonage, continu, détection des nouvelles barres.
 - Correction du calcul de la moyenne glissante pour les statistiques des pièces.
 - Corrections pour enregidtrer le temps de setup opérateur.

## LCD
v01.01.00:
- Mode Continu ajouté pour le nombrage du carrousel.
- Enregistrement et lecture des temps de setup opérateur sur la carte SD corrigé.
- Affichage de l'heure avec les secondes sur l'écran principal.
- Gestion de l'heure d'été / heure d'hiver.