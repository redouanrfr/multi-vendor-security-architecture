# 📋 Plan d'Adressage IP - Lab Multi-Vendor

## Vue d'ensemble

Ce document détaille le plan d'adressage du lab réseau multi-vendor composé de 6 sites interconnectés.

***

## 🌐 SITE 1 - Stormshield (Bleu)

**Firewall:** Stormshield-1  
**Rôle:** Site principal avec 3 segments réseau

| Réseau       | VLAN | Passerelle  | Hôtes     | Usage                           |
|--------------|------|-------------|-----------|---------------------------------|
| 40.40.1.0/24 | -    | 40.40.1.254 | 40.40.1.1 | VLAN USER                       |
| 40.40.2.0/24 | -    | 40.40.2.254 | 40.40.2.1 | VLAN GRE                        |
| 40.40.3.0/24 | -    | 40.40.3.254 | 40.40.3.1 | VLAN IPsec                      |
| 10.10.1.0/24 | -    | 10.10.1.254 | 10.10.1.1 | Interconnexion Firewall/Routeur |
| 10.10.2.0/24 | -    | 10.10.2.254 | 10.10.2.1 | Interconnexion Firewall/Routeur |

**Cloud externe:** 192.168.2.101 (Web StormShield)

***

## 🌐 SITE 2 - Stormshield (Bleu)

**Firewall:** Stormshield-2  
**Rôle:** Site secondaire avec 3 segments réseau

| Réseau       | VLAN | Passerelle  | Hôtes     | Usage                           |
|--------------|------|-------------|-----------|---------------------------------|
| 50.50.1.0/24 | -    | 50.50.1.254 | 50.50.1.1 | VLAN USER                       |
| 50.50.2.0/24 | -    | 50.50.2.254 | 50.50.2.1 | VLAN GRE                        |
| 50.50.3.0/24 | -    | 50.50.3.254 | 50.50.3.1 | VLAN IPsec                      |
| 20.20.1.0/24 | -    | 20.20.1.254 | 20.20.1.1 | Interconnexion Firewall/Routeur |
| 20.20.2.0/24 | -    | 20.20.2.254 | 20.20.2.1 | Interconnexion Firewall/Routeur |

**Cloud externe:** 192.168.2.100 (Web StormShield)

***

## 🌐 SITE 3 - FortiGate (Rouge)

**Firewall:** FortiGate  
**Rôle:** Routage et filtrage avec segment VPN

| Réseau       | VLAN | Passerelle  | Hôtes     | Usage                           |
|--------------|------|-------------|-----------|---------------------------------|
| 70.70.1.0/24 | -    | 70.70.1.254 | 70.70.1.1 | VNAL USER                       |
| 60.60.1.0/24 | -    | 60.60.1.254 | 60.60.1.1 | Interconnexion Firewall/Routeur |
| 60.60.2.0/24 | -    | 60.60.2.254 | 60.60.2.1 | Interconnexion Firewall/Routeur |

**Cloud externe:** 192.168.2.222 (Web Fortigate)

***

## 🌐 SITE 4 - Cisco FTD + FMC (Cyan)

**Firewall:** Cisco FTD 6.4.0-102  
**Management:** FMC 6.4.0-1  
**Rôle:** Site avec management centralisé Firepower

| Réseau         | VLAN | Passerelle    | Hôtes       | Usage                           |
|----------------|------|---------------|-------------|---------------------------------|
| 100.100.1.0/24 | -    | 100.100.1.254 | 100.100.1.1 | VLAN USER                       |
| 100.100.2.0/24 | -    | 100.100.2.201 | 100.100.2.1 | VLAN MGMT FTD                   |
| 111.111.1.0/24 | -    | 111.111.1.254 | 111.111.1.1 | Interconnexion Firewall/Routeur |
| 111.111.2.0/24 | -    | 111.111.2.254 | 111.111.2.1 | Interconnexion Firewall/Routeur |

**Management:**

-   FMC: 100.100.2.200
-   FTD: 100.100.2.201

**Cloud externe:** 192.168.2.227 (management web FMC)

***

## 🌐 SITE 5 - Cisco ASA (Cyan)

**Firewall:** Cisco ASA  
**Rôle:** Pare-feu traditionnel avec segmentation

| Réseau         | VLAN | Passerelle    | Hôtes       | Usage                |
|----------------|------|---------------|-------------|----------------------|
| 114.114.1.0/24 | -    | 114.114.1.254 | 114.114.1.1 | Segment utilisateurs |

**Cloud externe:** 192.168.2.132 (ASDM ASA)

***

## 🌐 SITE 6 - PaloAlto (Orange)

**Firewall:** PaloAlto 10.1-1  
**Rôle:** Next-Gen Firewall avec segmentation avancée

| Réseau       | VLAN | Passerelle  | Hôtes     | Usage       |
|--------------|------|-------------|-----------|-------------|
| 90.90.1.0/24 | -    | 90.90.1.254 | 90.90.1.1 | VLAN USER   |
| 90.90.2.0/24 | -    | 90.90.2.254 | 90.90.2.1 | VLAN SERVER |
| 80.80.1.0/24 | -    | 80.80.1.254 | 80.80.1.1 | FWALL/RTR   |
| 80.80.2.0/24 | -    | 80.80.2.254 | 80.80.2.1 | FWALL/RTR   |

**Cloud externe:** 192.168.2.229 (Web PaloAlto)

***

## 🔄 Réseau d'Interconnexion Central (Switch/Routeurs)

| Réseau       | Usage            | Équipements connectés |
|--------------|------------------|-----------------------|
| 30.30.1.0/24 | Backbone central | Tous les firewalls    |

**Détail des interfaces:**

-   30.30.1.1 - Routeur inter-site
-   30.30.1.2 - Routeur inter-site
-   30.30.1.3 - Routeur inter-site
-   30.30.1.4 - Routeur inter-site
-   

***

## 🔐 Réseau Management & Supervision

| Réseau         | Équipement  | IP            | Rôle             |
|----------------|-------------|---------------|------------------|
| 192.168.2.0/24 | Splunk      | 192.168.2.130 | SIEM             |
| 192.168.2.0/24 | FMC         | 192.168.2.227 | Management Cisco |
| 192.168.2.0/24 | Kali Linux  | 192.168.2.226 | Tests sécurité   |
| 192.168.2.0/24 | Fortigate   | 192.168.2.222 | MGMT WEB         |
| 192.168.2.0/24 | Stormshield | 192.168.2.101 | MGMT WEB         |
| 192.168.2.0/24 | Stormshield | 192.168.2.100 | MGMT WEB         |
| 192.168.2.0/24 | ASA         | 192.168.2.132 | MGMT ASDM        |
| 192.168.2.0/24 | PaloAlto    | 192.168.2.229 | MGMT WEB         |

***

## 📊 Synthèse par Vendor

### Cisco (FTD + ASA)

-   **Réseaux internes:** 100.100.x.0/24, 111.111.x.0/24, 114.114.1.0/24
-   **Total d'adresses:** \~768 IPs
-   **Management:** 192.168.2.227 (FMC), 192.168.2.201 (FTD)

### Stormshield

-   **Réseaux internes:** 40.40.x.0/24, 50.50.x.0/24, 10.10.x.0/24, 20.20.x.0/24
-   **Total d'adresses:** \~2048 IPs
-   **Sites:** 2 (Site 1 et Site 2)

### FortiGate

-   **Réseaux internes:** 70.70.1.0/24, 60.60.x.0/24
-   **Total d'adresses:** \~768 IPs
-   **Sites:** 1 (Site 3)

### PaloAlto

-   **Réseaux internes:** 90.90.x.0/24, 80.80.x.0/24
-   **Total d'adresses:** \~1024 IPs
-   **Sites:** 1 (Site 6)

***

## 🎯 Conventions de nommage

### Passerelles par défaut

-   Format: `X.X.X.254` pour tous les segments internes
-   Exceptions: Management FMC (X.X.X.200), FTD (X.X.X.201)

### Hôtes de test

-   Format: `X.X.X.1` pour le premier hôte de chaque segment
-   Utilisation: Validation connectivité et règles firewall

### Clouds WAN

-   Tous dans le réseau 192.168.2.0/24
-   Identification par numéro de cloud (Cloud1-Cloud8)

***

## 🔗 Technologies d'Interconnexion

| Technologie | Sites concernés  | Couleur diagramme |
|-------------|------------------|-------------------|
| SDWAN       | Tous les sites   | Bleu              |
| IPSec       | VPN site-to-site | Fuchia            |
| GRE         | Tunneling        | VERT              |

***

## 📝 Notes

-   Tous les réseaux sont en /24 pour simplifier la gestion
-   Réservation systématique de .254 pour les passerelles
-   Réseau 192.168.2.0/24 dédié au management et monitoring (remontés Splunk)
-   Segmentation par vendor pour faciliter le troubleshooting
-   Redondance assurée par multiples chemins d'interconnexion et multi-routes via routage dynamique RIPv2

***

**Dernière mise à jour:** Octobre 2024  
**Environnement:** GNS3 + Draw.io  
**Status:** Lab opérationnel ✅
