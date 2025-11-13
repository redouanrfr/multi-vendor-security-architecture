
# 🛠️ Scripts de Validation Sécurité Multi-Vendor

*Scripts de test et validation pour l'architecture de sécurité Fortinet, Cisco, Palo Alto, Stormshield*

---

## 📋 Scripts Disponibles

### 🔍 **Validation IPS & Détection**
- **[`ips-validation-tester.sh`](ips-validation-tester.sh)** - Tests légers de validation IPS
  - 🎯 Patterns Shellshock, Directory Traversal
  - 🔍 Scan de validation services
  - 📊 Génération comportement réseau

### 🛡️ **Validation Défense Complète**  
- **[`multi-vendor-security-validator.sh`](multi-vendor-security-validator.sh)** - Tests complets multi-vendor
  - 📡 Scan réseau légitime (baseline)
  - 🎯 Patterns détection (Shellshock, XSS, Traversal)
  - 🌊 Génération trafic légitime
  - 🔥 Validation règles firewall
  - 📈 Génération logs pour SIEM

---

## 🚀 Utilisation Rapide

```bash
# Donner les permissions d'exécution
chmod +x ips-validation-tester.sh
chmod +x multi-vendor-security-validator.sh

# Exécuter les tests
./ips-validation-tester.sh 192.168.1.100
./multi-vendor-security-validator.sh 192.168.1.100
