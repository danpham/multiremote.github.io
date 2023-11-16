Configuration du Raspberry Pi
=============================

# Serveur NTP
## Installation
```
sudo apt-get install ntp
```

## Configuration NTP

Le serveur adopte la configuration suivante pour diffuser l’heure de son horloge interne : 
```
nano /etc/ntp.conf
```
```
# /etc/ntp.conf, configuration for ntpd; see ntp.conf(5) for help

driftfile /var/lib/ntp/ntp.drift

# Leap seconds definition provided by tzdata
leapfile /usr/share/zoneinfo/leap-seconds.list

# Enable this if you want statistics to be logged.
#statsdir /var/log/ntpstats/

statistics loopstats peerstats clockstats
filegen loopstats file loopstats type day enable
filegen peerstats file peerstats type day enable
filegen clockstats file clockstats type day enable

server 127.127.1.0 burst prefer
fudge 127.127.1.0 stratum 0

# By default, exchange time with everybody, but don't allow configuration.
restrict -4 default kod notrap nomodify nopeer noquery limited
restrict -6 default kod notrap nomodify nopeer noquery limited

# Local users may interrogate the ntp server more closely.
restrict 127.0.0.1
restrict ::1

# Needed for adding pool entries
restrict source notrap nomodify noquery
```
L’heure locale du système est réglée sur le fuseau horaire Europe/Zurich (GMT+2).
```
sudo timedatectl set-timezone Europe/Zurich
```

## Configuration DHCP
### Installation
```
sudo apt install isc-dhcp-server
```
### Configuration
Fichier : nano /etc/dhcp/dhcpd.conf
```
default-lease-time 86400; # Bail de 24H
max-lease-time 172800; # Bail maxi de 48H
# Déclaration d'un réseau
subnet 192.168.0.0 netmask 255.255.255.0 {
        range                           192.168.0.30 192.168.0.35; # Plage IP
        option domain-name-servers      8.8.8.8; # DNS
        option routers                  192.168.0.10; # Passerelle
}
```

## Configuration adresses en IPv4
Dans le fichier /etc/sysctl.d/local.conf ajouter la ligne suivante :
```
net.ipv6.conf.all.disable_ipv6=1
```
