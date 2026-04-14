## 📌 Description – SAE3.03 Réseau Informatique & Multimédia

La SAE3.03 a pour objectif de moderniser une infrastructure réseau devenue obsolète, en remplaçant d’anciens serveurs (Windows Server 2008, Debian 7) par une architecture récente, sécurisée et adaptée aux besoins d’une entreprise moderne.  
Le projet consiste à concevoir, déployer et configurer un ensemble complet de services réseau, tout en respectant des contraintes réelles : virtualisation, adressage IP, sécurité, routage, WiFi professionnel, authentification centralisée et supervision.

L’ensemble de l’infrastructure repose sur deux machines virtuelles (Windows Server 2016 et Debian 11), un réseau physique configuré avec OSPF et VLAN, un point d’accès WiFi professionnel, et plusieurs services essentiels comme Active Directory, DNS, DHCP, Radius, Web et Zabbix.

---

### 🧩 **Résumé des services déployés**

| Service | Technologie | Rôle |
|--------|-------------|------|
| **Virtualisation** | VMware vCenter | Hébergement des VM Windows & Debian |
| **AD‑DS** | Windows Server 2016 | Gestion centralisée des utilisateurs et groupes |
| **DNS** | Intégré AD | Résolution de noms + sous‑domaine `etu10.sae` |
| **DHCP** | Switch Cisco (VLAN 11) | Attribution automatique d’adresses IP sécurisée |
| **Routage** | OSPFv2 | Communication entre réseau collaborateur et vCenter |
| **VLAN** | VLAN 11 | Isolation du réseau étudiant |
| **WiFi** | Ubiquiti UAP‑AC‑Lite | SSID Entreprise + SSID Invité |
| **Authentification** | RADIUS (NPS) | 802.1X pour le WiFi Entreprise |
| **Web** | IIS + Apache2 | Page web interne via sous‑domaine |
| **Supervision** | Zabbix | Monitoring des serveurs et équipements |
| **Veille technologique** | Zabbix / Grafana / VoIP | Analyse et étude de solutions professionnelles |

---

### 🏗️ **Ce que j’ai réalisé**

- Création et configuration des VM sous VMware (Windows Server + Debian).  
- Mise en place d’un domaine Active Directory complet (`etu10.sae`).  
- Configuration du DNS (zone directe, zone inverse, enregistrements A).  
- Déploiement d’un réseau physique avec deux routeurs Cisco et un switch.  
- Routage dynamique OSPF permettant l’accès aux services du vCenter.  
- Mise en place d’un VLAN dédié pour isoler le réseau collaborateur.  
- Déploiement d’un serveur DHCP sécurisé sur le switch.  
- Installation d’un point d’accès WiFi professionnel avec deux SSID :  
  - **Entreprise** (802.1X + RADIUS + filtrage)  
  - **Invité** (débit limité + accès restreint)  
- Configuration d’un serveur RADIUS (NPS) lié à l’Active Directory.  
- Hébergement d’une page web interne via IIS et Apache2.  
- Installation et configuration de Zabbix pour superviser l’infrastructure.  
- Réalisation d’une veille technologique sur la supervision et la téléphonie VoIP.

---

### 🎯 **Objectif final**

L’objectif de la SAE3.03 est de produire une infrastructure réseau **fiable**, **sécurisée**, **documentée**, et **fonctionnelle**, capable de répondre aux besoins d’une entreprise moderne :  
authentification centralisée, services réseau robustes, WiFi professionnel, supervision, segmentation et routage dynamique.

Ce projet représente une mise en situation réelle du métier d’administrateur réseau.
