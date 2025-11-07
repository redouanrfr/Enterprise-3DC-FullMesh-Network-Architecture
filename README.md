# 🚀 Infrastructure 3DC Full-Mesh Haute Disponibilité

[![Production](https://img.shields.io/badge/STATUS-EN%20PRODUCTION-00a550?style=for-the-badge)](https://en.wikipedia.org/wiki/Production_environment)
[![GNS3](https://img.shields.io/badge/Validé%20sur-GNS3-2a4d69?style=for-the-badge&logo=cisco)](https://www.gns3.com/)
[![Full-Mesh](https://img.shields.io/badge/🏗️-Full--Mesh_Certified-FF6B35?style=for-the-badge)]()
[![HA](https://img.shields.io/badge/⚡-HA_99.99%25-00D26A?style=for-the-badge)]()
[![DR](https://img.shields.io/badge/🌪️-Total_Disaster_Recovery-8B0000?style=for-the-badge)]()

## 🛠️ Technologies Employées

[![BGP](https://img.shields.io/badge/BGP-eBGP/iBGP-F27173?style=flat-square&logo=cisco)]()
[![HSRP](https://img.shields.io/badge/HSRP-Triple_HSRP-0096D6?style=flat-square&logo=cisco)]()
[![Cisco-ASA](https://img.shields.io/badge/Cisco_ASA-HA_Cluster-1BA0D7?style=flat-square&logo=cisco)]()
[![FortiGate](https://img.shields.io/badge/FortiGate-HA_Cluster-EE3124?style=flat-square)]()
[![MAN](https://img.shields.io/badge/MAN-Ethernet_L2-7E57C2?style=flat-square)]()
[![VLAN](https://img.shields.io/badge/VLAN-Trunk_802.1Q-4CAF50?style=flat-square)]()
[![STP](https://img.shields.io/badge/STP-Spanning_Tree-FF9800?style=flat-square)]()
[![Reverse-Proxy](https://img.shields.io/badge/Reverse_Proxy-Load_Balancing-9C27B0?style=flat-square)]()
[![Multi-DC](https://img.shields.io/badge/Multi--DC-3_Sites-FF6D00?style=flat-square)]()

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
[📥 Télécharger la démonstration](Demos/Bascule.BGP.FULL.AUTO.mp4) - *Cliquez puis "Download raw"*
**Scénario** : Coupure du routeur principal Paris-Bag  
**Démonstration** : Basculement automatique vers le routeur secondaire Noisiel  
**Protocoles** : BGP + HSRP  
**Temps** : Basculement automatique sans intervention 4min30s

### 2. Redondance Serveurs  
[📥 Télécharger la démonstration](Demos/Redondance-Bascule-Totale-des-serveurs-vers-site-de-secours.mp4) - *Cliquez puis "Download raw"*
**Scénario** : Basculement complet des serveurs vers le site de secours  
**Démonstration** : Migration transparente des services  
**Mécanisme** : HSRP + re-routage automatique  
**Impact** : Aucune interruption de service réseau

### 3. Disaster Recovery Complet
[📥 Télécharger la démonstration](Demos/Disaster.Recovery-Site.Paris-to-Site.Noisiel.mp4) - *Cliquez puis "Download raw"*
**Scénario** : Extinction totale du site Paris-Bag  
**Démonstration** : Basculement complet vers Noisiel en 4min30  
**RTO Mesuré** : 4 minutes 30 secondes  
**Couverture** : Routeurs, firewalls, serveurs, connectivité

*Note : Les vidéos doivent être téléchargées pour être visionnées*
