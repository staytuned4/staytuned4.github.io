---
layout: default
title: network
tags: [réseau, plage IP, glossaire]
---
# {{ page.title }}

|		|Class|		|IPV4 (4 octets)|Plage|Masque par défaut|IP reservé aux réseaux locaux-LAN (IP non routables)|*-2 postes (n°de réseau et broadcast)|Réservé|
|--|-|-------|-------|-------------------|
|GR|A|0 à 127|x.X.X.X|0.X.X.X à 127.X.X.X|255.0.0.0 ou /8 (1 octet)|10.X.X.X|1 réseau de 256<sup>3</sup> (65 536) postes*|0.X.X.X à 127.X.X.X|
|MR|B|128 à 191|x.x.X.X|128.0.X.X à 191.255.X.X|255.255.0.0 ou /16 (2 octets)|172.16.X.X à 172.31.X.X|16 réseaux de 256<sup>2</sup> postes*|169.254.X.X|
|PR|C|192 à 223|x.x.x.X|192.0.0.X à 223.255.255.X|255.255.255.O ou /24 (3 octets)|192.168.0.X à 192.168.255.X|256 réseaux de 256 postes*||
||D|||224 à 239|255.255.255.254 ou /31|
||E|||240 à 255|


# GR MR PR
Grand, Moyen, Petit réseau.

# Broadcast
Pour parler à tout le monde.

# Locale host
Boucle locale.

# APIPA
Fonction windows, assigne adress IP de class B entre 169.254.0.0 et 169.254.255.255 lorsqu'un serveur DHCP est indisponible.

# DHCP
Dynamic Host Configuration Protocol (réservation d'address IP – PC demande address IP, dhcp vérifie adresse allouée – 2 tables : dynamique/statique. Sinon il donne une adresse dynamique).
Configurer dhcp : Dynamique – reglé par l'ordi - “auto” pr le poste client. Statique : attribut adresse mac et ip. Dhcp évite donc d'entrer toutes les adresses des machines ds le NAT – 1 carte réseau = 1 IP

# DNS
Domain Name System (traduit un nom en address ip – et vice versa. PC demande au dns de traduir nom en adresse ip, dns regarde ds sa base si il a la réponse, sinon le dns demande à un autre dns etc etc).

# FTP
File Transfert Protocol

# AD
Active Directory (Annuaire-type LDAP) Administrer des comptes utilisateurs et ordinateur – c a d donner ou restreindre les droits des personnes et contrôler ce que font les personnes et les ordinateurs. Infos sur les personnes et les machines ainsi que les droits

# SAMBA
Intégrer des réseaux autre que windows dans un réseau et/ou un domaine sous windows.

# RADIUS
Permet d'authentifier un poste distant pour lui permettre d'avoir un accès au réseau de l'entreprise.

# IP
Internet Protocol – IP routable = sur le net (IP réservé aux réseaux locaux = non routable) 

# Loopback
(boucle locale)  127.0.0.1 interface fictive sur toute les machine – permet à la machine de s'envoyer des paquets ex: test site internet

# NAS
Network Attached Storage (Serveur de stockage en réseau)

# NAT 
Network Address Translation (PASSERELLE = Gateaway) - permet de connecter 2 réseaux qui n'utilisent pas les mêmes protocoles de communications ex: Ethernet, Uni, Telway...
1 Passerelle → 1 réseau

# Subnet
1ère adresse réseau

# PONT
permet de connecter 2 réseaux qui utilisent les même protocoles de communications

# PARE-FEU
Gère les protocoles de communications entrée/sortie – protège PC du réseau – pare-feu sous Linux car possibilité de redémarrer uniquement le service et non tout le serveur.

# MODEM
traduit analogique en numérique (et vice versa)

# ROUTEUR
(= passerelle, router, gateway) : Box sans modem
Dirige l'info – machine avec mini 2 cartes réseaux (2 ip) avec interconnexion entre les cartes

# Modem routeur
Box

# CONCENTRATEUR
(HUB ou SWITCH)
HUB envoie à tout le monde – 1 seul connexion
SWITCH dirige l'info – concentrateur intelligent – connexion simultanée (besoin de mémoire-donc prix).

# Table de Routage
Savoir sur chaque port ce qu'il y a.

# Plan d'adressage
telle machine a tel IP

# DMZ
zone entre 2 routeurs – où l'on peut mettre : Serveur web, Serveur Mail, Bastion.

# BASTION
machine (peut être virtuelle) qui attire toutes les attaques internet (honey-pot)

# Différentes typologie de réseaux
Bus, Anneau (pas de perte d'info-payant), Etoile (débit important-gratuit), Maillé (point à point)
Bus obsolète (débit faible)-Anneau (1 seul PC communique à la fois).

# LAN
Local Area Network - group of computers that share a common connection in small area or same building (wlan Wireless Local Area Network)
MAN Metropolitan Area Network – larger network that connects computers in a particular geographique area or region Ex: univiversity with network so large that it's classified as MAN 
WAN Wide Area Network – largest network, can interconnect networks – not restricted to geographical  location – internet = WAN

# Carte réseau
3ème chiffre = fabricant – les autres chiffres = ref de la carte

# Clés wifi
(Maj, minuscule et chiffre – mini 13 carractères), WPA et WPA2 (Tous les carractères – mini 16 carractères + est généré une clé qui change régulièremment – ce qui peut provoquer déconnexion)

# Serveur mutualisé
1 machine, plusieurs site internet

# 100 base T
(débit en megabit, ethernet, type de cable) – Torsadé/Fibre/2 (coaxial-1Gb sur 100 mètre)

# Réseau
1ère adresse = réseau, dernière adresse = adresse de diffusion ou broadcast (pr parler à tout le monde).

# APIPA
(voir dhcp) adresse permettant à des machines à communiquer automatiquement: connexion réduite ou inéxistante (pas de dhcp-serveur web).

# Traceroute
(Tracert) + URL : indique le chemin (peut changer selon encombrement)

# ARP (requête)
travail au niveau des ports

# RJ45
(voyant) : allumé, bien branché (matériel) – clignote, transmission (logique, communication)

# RAM Random Access Memory
mémoire vive – Statique (la donnée est mise et reste) ou Dynamique (+ rapide mais obligation de rafraîchir).

# Microprocesseur
(MP) permet de faire des calculs – horloge, vitesse à laquelle il travail

# BIOS
(ROM) Basic Input Output System (System élémentaire d'entrée/sortie – situé ds ROM) – logiciel contrôlant la carte mère – flashé Bios = amélioration de la carte mère.

# SETUP
(RAM) configuration matériel du PC – pile lithium garde Setup en mémoire.

# CHIPSET
(Pont Nord, appareil rapide ou Sud, appareil lent) gère tout les périphériques connectés au microprocesseur (MP, RAM, ROM, interface entrée).

# DRAM
Dynamic Random Access Memory

# EPROM
Erasable Programmable Read-Only Memory

# EEPROM
Electrically-Erasable Programmable Read-Only Memory

# ROM
Read Only Memory – mémoire morte

# USB
Universal Serial Bus

# IDE
Integrated Drive Electronics

# AGP
Accelerated Graphics Ports

# PCI
Peripheral Component Interconnect 

# SATA (série)
Serial Advanced Technology Attachment

# PATA (parallèle)
Type de socket : défini le type du MP
Port Série: envoie 0 et 1 les uns après les autres.
Port Parallèle: envoie 0 et 1 en même temps.

# Linux
base Unix comme Mac OS – origine libre et open source – 1 configuration = 1 fichier texte. Windows est propriétaire

# Migration
faire évoluer OS vers OS du même fabricant

# Installation
Remise DD à 0 – installation de l'OS

# Formatage bas niveau
(d'usine) ≠ formatage logique.
Partition principale : limitée à 4 partitionnements.
Partition étendue : + de 4 parttions.

# émuler
simuler une puce par un logiciel

# Unicat
1 seul Machine / Broadcast = Plusieurs machines

# IPV4
4 octets 0-255 (256 valeurs) – 16 millions de possibilités – réseau interne (locaux)

# IPV6
16 octets (créé pr internet – ipv4 saturé)

# Ping
frappe à la porte d'un site – ex: ping yahoo.fr / pr tester le NAT, DNS.

# Proxy
site mandataire

# calcul IP pour faire communiquer 2 PC :
PC1 puisse voir PC2 : IP1 . M1 = IP2 . M1
PC 2 puisse voir PC1 : IP1 . M2 = IP2 .M2

-2 postes (1: no du réseau, 2: pr parler à tout le monde Broadcast).

# Masque
autorise ou empêche machine à comuniquer entre elle. Remplacé par annuaire (+ simple à gérer) via le compte utilisateur. Pb si server annuaire tombe en panne (il y a 1 de secoure). 

# Masque de reseau et masque de sous réseau ???? à voir
Ex : 192.168.10.2/24 (nb de bit à 1 ds le masque) – 24 = 3X8 donc 8 “1” ds masque (class C) donc 255.255.255.0 (11111111-11111111-11111111-00000000)

802.11 wifi / 802.5 bluetouth / 802.11 securisation réseau (info à vérifier)
WAN (ip public)	–	NAT	–	 LAN (ip privée)

# port ouvert par défaut ds windows
telnet,part feu rfc, ftp, smtp, pop,dns, http, https, port443...

# ports principaux d'un pare-feu
dhcp, 67 68, mysql...
(certain ports ont une fonction d'autres n'en ont pas)
voir liste des ports TOP et UDP (comment les désactivés – frameip.com)

<!--Ds XP tous les comptes sont Admin
Ds 7 et 8 aucun comptes (Admin avec droits)

antivirus : BitDefender, Karpersky...
suprimer virus (+ sûr)
virus: infecte les machines – rends PC inutilisable – Antivirus.
Malware : Ouvre fenêtre non désirée – Pub – AntiMalware.
Cheval de troie : Prends contrôle de la machine.

Partage Imprimante (windows) :
Installer : Démarrer – Imprimante et télécopieur – Ajouter une imprimante
Pr que l'imprimante soit visible sur le réseau : “Partager” (10 postes maxi) – Idem pr Répertoire
port Lpt1 : pr partager imprimante - “si vs êtes conscient...” -  ok

Partage Dossier :
Créer Dossier – Clic D – Partager – Sélectionner “si les autres peuvent lire et ou modifier le contenu du dossier” (à faire en utilisateur normal – pr éviter de se logger en admin)

Driver générique (Vérifier si) : Démarrer – Clic D  sur Poste de travail – Gérer – MAJ de Chipset – Redémarer (windows trouve enfin Driver récent pr la carte graphique)

Fragmentation : mettre tout ensemble

Dos – DosShell (poste de travail en mode console), mc sous Linux – Poste de Travail -->


