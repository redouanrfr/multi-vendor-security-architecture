# Multi-Vendor Security Architecture Portfolio

![Multi-Vendor Security](https://img.shields.io/badge/Architecture-Multi--Vendor_Security-blue)
![Firewalls](https://img.shields.io/badge/Technology-Firewalls%20%7C%20IPS%20%7C%20SIEM-green)
![Lab Environment](https://img.shields.io/badge/Platform-GNS3%20%7C%20Kali%20Linux-orange)
![RIP Backbone](https://img.shields.io/badge/Backbone-4_Routeurs_RIPv2_Simulateur_Internet-FF6B35)
![Testing](https://img.shields.io/badge/Tests-Security%20%7C%20Failover%20%7C%20IPS-red)

## 📖 Description du Projet

Architecture de sécurité multi-vendor complète simulant un environnement d'entreprise avec 6 sites interconnectés via un backbone de 4 routeurs RIPv2. Ce laboratoire démontre l'interopérabilité entre solutions Fortinet, Cisco, Palo Alto et Stormshield avec supervision centralisée Splunk SIEM.

## 🛠️ Technologies Employées

### 🔥 Firewalls & Sécurité Multi-Vendor
[![Fortinet](https://img.shields.io/badge/Fortinet-FortiGate_SD--WAN_IPS_Application_Control-EE3124?style=flat-square&logo=fortinet)]()
[![Cisco ASA](https://img.shields.io/badge/Cisco_ASA-IP_Tracking_Stateful_Firewall-1BA0D7?style=flat-square&logo=cisco)]()
[![Cisco FTD](https://img.shields.io/badge/Cisco_FTD-Firepower_Threat_Defense-005073?style=flat-square&logo=cisco)]()
[![Cisco FMC](https://img.shields.io/badge/Cisco_FMC-Firepower_Management_Center-0080A4?style=flat-square&logo=cisco)]()
[![Palo Alto](https://img.shields.io/badge/Palo_Alto-NGFW_Threat_Prevention-00a0e9?style=flat-square)]()
[![Stormshield](https://img.shields.io/badge/Stormshield-SNS_Firewall_SD--WAN-005CA9?style=flat-square)]()

### 🌐 Backbone & Interconnexion
[![RIP Backbone](https://img.shields.io/badge/Backbone-4_Routeurs_RIPv2_Simulateur_Internet-FF6B35?style=flat-square&logo=router)]()
[![SD-WAN](https://img.shields.io/badge/SD--WAN-Failover_<5s_SLA_Monitoring-7E57C2?style=flat-square)]()
[![IPSec](https://img.shields.io/badge/IPSec-Tunnels_Cryptographiques-4CAF50?style=flat-square)]()
[![GRE](https://img.shields.io/badge/GRE-Tunnels_Séparés_IPSec-8BC34A?style=flat-square)]()

### 🔍 Monitoring & Testing
[![Splunk](https://img.shields.io/badge/Splunk-SIEM_Corrélation_Multi--vendor-79B443?style=flat-square)]()
[![Kali Linux](https://img.shields.io/badge/Kali_Linux-Tests_Intrusion_IPS_Detection-557C94?style=flat-square&logo=kalilinux)]()
[![Wireshark](https://img.shields.io/badge/Wireshark-Analyse_GRE_vs_ESP-1679A7?style=flat-square)]()

### 🏗️ Platform & Virtualisation
[![GNS3](https://img.shields.io/badge/GNS3-Lab_6_Sites_Multi--vendor-2a4d69?style=flat-square&logo=cisco)]()
[![ESXi](https://img.shields.io/badge/VMware_ESXi-Virtualisation_Hyperviseur-607D8B?style=flat-square)]()

## 🧪 Tests Réalisés
- **SD-WAN Tests Failover** sur backbone RIPv2
- **Test Routage dynamique** avec convergence RIP
- **Multi-Vendor IPS Testing** via Kali Linux
- **SIEM Splunk Correlation** logs multi-sources
- **Advanced VPN (IPsec, GRE)** traversant le backbone
- **Cisco ASA IPtracking SLA** 
- **GNS3 Lab Environment** 6 sites

## 📚 Documentation
- [📋 Plan d'adressage IP complet](lab-documentation/addressing_plan.md)
- [📄 Diagramme réseau (PDF)](lab-documentation/multi-vendor-firewall-ips-splunk-architecture.pdf)

## 🎬 Démonstrations Vidéo

### 📁 [Dossier des Démonstrations Complètes](./demonstrations/)

**7 démonstrations techniques :**
- 🏰 SD-WAN Fortigate - Failover automatique <5s
- 🌪️ SD-WAN Stormshield - Routage dynamique intégré
- ⚔️ IPS Multi-Vendor - Tests Kali + corrélation Splunk
- 🔒 Tunneling Avancé - IPsec & GRE séparés
- 🔧 Intégration FTD - Cisco Firepower Management Center
- 🔍 IP Tracking Cisco - Résilience multi-WAN
- 🛠️ Environnement Lab - Démarrage complet infrastructure

*[Voir toutes les démonstrations détaillées]( /demonstrations/README.md)*

## 🛠️ Technologies
- **Firewalls**: Fortinet, Cisco ASA/FTD, Palo Alto, Stormshield
- **Supervision**: Splunk SIEM
- **Réseau**: SD-WAN, IPSec, GRE, RIPv2 Backbone
- **Testing**: Kali Linux, SLA Monitoring
- **Topologie**: 6 sites interconnectés via 4 routeurs RIPv2

---

**🏆 Portfolio Technique** - Architecture de sécurité enterprise réaliste avec backbone RIPv2 et intégration multi-vendor complète.
