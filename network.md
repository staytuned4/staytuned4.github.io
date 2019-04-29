---
layout: default
title: network
tags: [réseau, plage IP]
---
# {{ page.title | capitalize }}

|		|Class|		|IPV4 (4 octets)|Plage|Masque par défaut|IP reservé aux réseaux locaux-LAN (IP non routables)|*-2 postes (n°de réseau et broadcast)|Réservé|
|--|-|-------|-------|-------------------|
|GR|A|0 à 127|x.X.X.X|0.X.X.X à 127.X.X.X|255.0.0.0 ou /8 (1 octet)|10.X.X.X|1 réseau de 256<sup>3</sup> (65 536) postes*|0.X.X.X à 127.X.X.X|
|MR|B|128 à 191|x.x.X.X|128.0.X.X à 191.255.X.X|255.255.0.0 ou /16 (2 octets)|172.16.X.X à 172.31.X.X|16 réseaux de 256<sup>2</sup> postes*|169.254.X.X|
|PR|C|192 à 223|x.x.x.X|192.0.0.X à 223.255.255.X|255.255.255.O ou /24 (3 octets)|192.168.0.X à 192.168.255.X|256 réseaux de 256 postes*||
||D|||224 à 239|255.255.255.254 ou /31|
||E|||240 à 255|


## GR MR PR
Grand, Moyen, Petit réseau.

## Broadcast
Pour parler à tout le monde.
## Locale host
Boucle locale.
## APIPA
Fonction windows, assigne adress IP de class B entre 169.254.0.0 et 169.254.255.255 lorsqu'un serveur DHCP est indisponible.
