# 🚀 Infrastructure 3DC Full-Mesh Haute Disponibilité

[![Production](https://img.shields.io/badge/STATUS-EN%20PRODUCTION-00a550?style=for-the-badge)](https://en.wikipedia.org/wiki/Production_environment)
[![GNS3](https://img.shields.io/badge/Validé%20sur-GNS3-2a4d69?style=for-the-badge&logo=cisco)](https://www.gns3.com/)

**Infrastructure réseau full-mesh multi-datacenters déployée en production**

---

## 🏗️ Architecture Déployée

### **Sites en Production**
- **Paris-Bag** : Site principal (Production)
- **Noisiel** : Site de DR (Disaster Recovery)  
- **PA6** : Site de backup

### **Technologies Clés**
- **Full-Mesh** : Topologie triangle via MAN Ethernet
- **BGP** : eBGP avec dual ISP + iBGP interne (AS 65001)
- **HA** : HSRP triple + Clusters firewall (ASA & FortiGate)
- **Sécurité** : Parcours contrôlé Internet → ASA → FortiGate → Serveurs

---

## ⚡ Résultats Validés

### **Tests de Basculement**
| Scénario | Résultat | Temps |
|----------|----------|-------|
| Failover site Paris-Bag | ✅ Réussi | HSRP instantané |
| Panne Router-A | ✅ Réussi | BGP 4min30s |
| DR complet | ✅ Réussi | RTO 4min30s |

---
## 🎥 Démonstrations Vidéo

### 1. Basculement BGP Automatique
[![Basculement BGP](https://img.shields.io/badge/🎥-Voir_la_démonstration-blue)](Demos/Bascule.BGP.FULL.AUTO.mp4)
**Scénario** : Coupure du routeur principal Paris-Bag  
**Démonstration** : Basculement automatique vers le routeur secondaire Noisiel  
**Protocoles** : BGP + HSRP  
**Temps** : Basculement automatique sans intervention 4min30s

### 2. Redondance Serveurs  
[![Redondance Serveurs](https://img.shields.io/badge/🎥-Voir_la_démonstration-green)](Demos/Redondance-Bascule-Totale-des-serveurs-vers-site-de-secours.mp4)
**Scénario** : Basculement complet des serveurs vers le site de secours  
**Démonstration** : Migration transparente des services  
**Mécanisme** : HSRP + re-routage automatique  
**Impact** : Aucune interruption de service réseau

### 3. Disaster Recovery Complet
[![Disaster Recovery](https://img.shields.io/badge/🎥-Voir_la_démonstration-red)](Demos/Disaster.Recovery-Site.Paris-to-Site.Noisiel.mp4)
**Scénario** : Extinction totale du site Paris-Bag  
**Démonstration** : Basculement complet vers Noisiel en 4min30  
**RTO Mesuré** : 4 minutes 30 secondes  
**Couverture** : Routeurs, firewalls, serveurs, connectivité

