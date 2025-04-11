# 🔐 MiniProjet SSL/TLS

Ce mini-projet présente une exploration complète du protocole SSL/TLS, son fonctionnement, ses vulnérabilités, ainsi que les bonnes pratiques de configuration.

## 👥 Réalisé par
- Hamza AIT LAMAALAM  
- Nadir ALMELLOUKI  
- Mohammed ABIDOU  
- Saad ADDAR  
- Omar ANOUAR  

## 🧠 Contenu du Projet

### 1. Introduction
Présentation des objectifs de sécurité de SSL/TLS : confidentialité, intégrité, et authentification.

### 2. Fonctionnement de SSL/TLS
Explication du handshake TLS, des certificats numériques, de la cryptographie asymétrique et symétrique.

### 3. Évolution des Protocoles
Comparaison entre SSL 1.0 → TLS 1.3, avec mise en lumière des failles et des améliorations.

### 4. Types de Certificats
Analyse des certificats DV, OV, EV, Wildcard & Multi-Domain (SAN).

### 5. Utilisations de TLS
- HTTPS  
- Emails (SMTP, IMAP, POP3)  
- VPN & Cloud (OpenVPN, WireGuard)

### 6. Vulnérabilités & Attaques
- Man-in-the-Middle  
- POODLE  
- BEAST, DROWN, Heartbleed, CRIME/BREACH  

### 7. Bonnes Pratiques & Outils
- Désactivation des versions obsolètes (SSL 3.0, TLS 1.0/1.1)  
- Utilisation d’outils : SSL Labs, OpenSSL, Wireshark  

## ⚙️ Exemple de Configuration (Apache)

```bash
sudo apt update && sudo apt install apache2
sudo ufw allow 'Apache Full'
sudo a2enmod ssl
# Génération de certificat auto-signé
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/apache-selfsigned.key -out /etc/ssl/certs/apache-selfsigned.crt
