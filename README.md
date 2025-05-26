🌌 StellarUDP

    Développé par StellarBots123 — Membre de la team [Stellar-iot]

🚀 StellarUDP est un outil d’envoi massif de paquets UDP spoofés, écrit en Go, conçu pour tester la résilience réseau. Léger, rapide, sans dépendance à libpcap, il permet de simuler des charges réseau réalistes à partir d’un bloc IP spécifique.
✨ Fonctionnalités

    🔥 Envoi ultra-rapide de paquets UDP

    🎭 Spoofing IP dans le bloc 212.64.201.0/24

    🧱 Construction manuelle des entêtes IP + UDP (raw socket)

    ⏳ Contrôle complet via 4 arguments : IP cible, port, durée, taille paquet

    💻 100% Go — aucun outil externe requis

⚙️ Compilation

git clone https://github.com/StellarBots123/StellarUDP.git
cd StellarUDP
go build -o flood flood.go

🚀 Utilisation

sudo ./flood <IP_CIBLE> <PORT> <DUREE_SECONDES> <TAILLE_PACKET>

Exemple :

sudo ./flood 192.250.230.103 1337 60 1024

Argument	Description
IP_CIBLE	L’adresse IP cible
PORT	Port UDP de destination
DUREE_SECONDES	Durée d’exécution du flood (ex : 60)
TAILLE_PACKET	Taille de chaque paquet (ex : 1024 octets)
📤 Exemple de sortie

[+] Cible : 192.250.230.103
[+] Port : 1337
[+] Durée : 60 secondes
[+] Taille paquet : 1024 octets
[+] Bloc généré avec 256 IP spoofées.
[+] IP spoofée : 212.64.201.1
...
[+] Terminé après 60 secondes.

📘 Aide intégrée dans le code

if len(os.Args) != 5 {
	fmt.Println("📘 Usage: sudo ./flood <IP_CIBLE> <PORT> <DUREE_SECONDES> <TAILLE_PACKET>")
	fmt.Println("Exemple: sudo ./flood 192.250.230.103 1337 60 1024")
	return
}

⚠️ Avertissement légal

    ❗ StellarUDP est un outil à usage éducatif et de test uniquement.
    Toute utilisation sur des réseaux ou machines sans autorisation explicite est illégale et interdite.
    Vous êtes seul responsable de son usage.

💡 To-do

Option --quiet pour désactiver l'affichage

Support TCP/ICMP spoofé

Ajout d'autres blocs IP configurables

    Interface CLI interactive

👨‍💻 Auteur

    👾 Projet créé par StellarBots123
    🛰️ Membre de la team Stellar-iot
    🔗 GitHub
