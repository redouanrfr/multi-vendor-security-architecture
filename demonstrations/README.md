# 🎬 Démonstrations Vidéo
Dossier des démonstrations techniques multi-vendor.

## 📋 Catalogue des Démonstrations

### 🏰 **`test-sd-wan-fortigate.mp4`** - Implémentation SD-WAN Fortinet avec :Test SD-WAN & Performance
  - **Performance SLA** : Monitoring temps réel (latence, jitter, perte de paquets)
  - **Health-checks multi-liens** : Vérification continue de l'état des connexions
  - **Routage dynamique RIP** : Recalcul automatique des routes en cas d'incident
  - **Failover automatique <5s** : Test de résilience avec arrêt du routeur WAN 1 → bascule transparente vers WAN 2
  - **Bascule 5 secondes** : Validation du temps de reprise après coupure complète

### 🌪️ **`test-sd-wan-stormshield.mp4`** - Stormshield **SD-WAN Built-in** avec routage dynamique :
  - **SD-WAN intégré** : Utilisation des fonctionnalités SD-WAN natives Stormshield
  - **Architecture multi-gateway** : 
    - Routeur Internet 1 (ACTIVE) → WAN 1
    - Routeur Internet 2 (STANDBY) → WAN 2
  - **SD-WAN SLA thresholds** : Configuration des seuils de performance et health-checks
  - **Active/Backup Gateway** : Mécanisme de basculement hiérarchisé géré par le SD-WAN
  - **Test de résilience SD-WAN** : Arrêt routeur 1 → bascule automatique immédiate vers routeur 2 via SD-WAN
  - **Routage dynamique RIP** : Intégration du SD-WAN avec recalcul automatique des tables de routage
  - **Rétablissement automatique** : Redémarrage routeur 1 → retour à la configuration SD-WAN initiale
  - **Link Optimization** : Optimisation des chemins via politiques SD-WAN

###  ⚔️ **`test-kali-ips-logs-splunk.mp4`** - Tests d'intrusion Kali Linux avec corrélation logs multi-vendor (Fortinet, Cisco, Palo Alto, Stormshield) dans Splunk
  - Démarrage complet de l'infrastructure lab.
  - **Infrastructure hôte** : Démarrage et configuration de la machine physique hébergeant ESXi
  - **Hyperviseur ESXi** : Mise en service de la plateforme de virtualisation
  - **GNS3** : Démarrage de l'environnement de simulation réseau avec topologie 5 sites
  - **VM Splunk** : Démarrage de la machine virtuelle Splunk Enterprise
  - **Connectivité cloud** : Configuration de la communication entre Splunk et le lab GNS3 via connexion cloud
  - **Démarrage firewalls** : Séquence de boot et initialisation de tous les firewalls :
    - FortiGate, Cisco FTD, Palo Alto, Stormshield
  - **Établissement tunnels** : Création des tunnels GRE et IPsec entre les deux Stormshield (voir tunneling ipsec et gre.mp4)
  - **Validation connectivité** : Vérification de la communication via monitoring Stormshield et outils intégrés
   🛡️⚔️📊 Le test IPS multi-vendor car il combine sécurité offensive, remontée de logs et intégration SIEM - trois compétences critiques en cybersécurité moderne.
    
###  🔒📦 **`tunneling-ipsec-gre.mp4`** - Tunnels IPsec et GRE séparés entre Stormshield avec validation protocolaire :
  - **Tunnel GRE distinct** : Configuration et établissement d'un tunnel GRE dédié
  - **Tunnel IPsec distinct** : Configuration et établissement d'un tunnel IPsec séparé
  - **Validation GRE** : Tests ICMP via tunnel GRE → analyse Wireshark confirmant le protocole GRE dans les captures
  - **Validation IPsec** : Tests ICMP via tunnel IPsec → analyse Wireshark montrant le traffic ESP (Encapsulating Security Payload)
  - **Analyse comparative** : Inspection Wireshark pour différencier :
    - Trafic GRE (protocol 47) avec encapsulation visible
    - Trafic IPsec/ESP (protocol 50) avec payload chiffré
  - **Vérification intégrité** : Confirmation que chaque tunnel fonctionne indépendamment et transmet correctement le trafic
    
### 🔧 Intégration & 🔍 Monitoring
- **`adding-ftd-fmc.mp4`** - 🔧Intégration Cisco Firepower Threat Defense dans l'architecture existante
   - **`lab-ip-tracking-cisco.mp4`** - IP Tracking 🔍 avancé Cisco ASA avec résilience multi-WAN :
  - **Implémentation Cisco** : Configuration basée sur la documentation Cisco officielle [ASA IP Tracking]
    (https://www.cisco.com/c/en/us/support/docs/security/asa-5500-x-series-next-generation-firewalls/118962-configure-asa-00.html)
  - **Route statique avec tracking** : 
    - Next hop : Routeur 4 (actif via interface WAN 1)
    - Métriques par défaut avec monitoring continu
  - **Test de résilience** : Coupure volontaire du Routeur 4 (next hop de la route par défaut)
  - **Bascule automatique <5s** : Transition transparente vers WAN 2 et Routeur 2 via route de backup
  - **Routage dynamique RIP** : Mise à jour automatique des tables de routage sur tous les routeurs du domaine RIP
  - **Rétablissement automatique** : Remise en service du Routeur 4 → retour à la normale avec restauration de la route par défaut WAN 1
  - **Validation complète** : Vérification du bon fonctionnement avant/après bascule et après rétablissement

## 🎬 Comment Visionner
Cliquez sur chaque fichier vidéo, puis sur "Download" pour visualiser la démonstration.

*Toutes les démonstrations incluent un watermark de protection.*
