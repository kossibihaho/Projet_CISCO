# Projet_CISCO
Conception et simulation du réseau sécurisé d’une entreprise multi-départements basé sur une architecture hiérarchique avec redondance.


# 🌐 Conception et simulation d'un réseau d'entreprise sécurisé avec Cisco Packet Tracer

![Cisco](https://img.shields.io/badge/Cisco-Networking-049fd9?logo=cisco&logoColor=white)
![Packet Tracer](https://img.shields.io/badge/Simulation-Packet%20Tracer-blue)
![Networking](https://img.shields.io/badge/Domain-Network%20Engineering-orange)
![Status](https://img.shields.io/badge/Status-Academic%20Project-success)

## 📌 Présentation du projet

Ce projet consiste à concevoir et simuler l'infrastructure réseau d'une entreprise organisée en plusieurs départements, en s'appuyant sur une architecture réseau hiérarchique, sécurisée et redondante.

L'objectif est de mettre en place une infrastructure capable de répondre aux besoins d'une entreprise moderne : assurer la communication entre les différents services, segmenter le réseau, contrôler les échanges de données et garantir la continuité des services en cas de défaillance de certains équipements.

La conception et la simulation sont réalisées avec **Cisco Packet Tracer**, afin de reproduire un environnement réseau d'entreprise et de vérifier le fonctionnement des différents mécanismes configurés.

## 🏢 1. Contexte et problématique

Une entreprise possédant plusieurs départements doit disposer d'une infrastructure réseau fiable permettant à ses collaborateurs d'accéder aux ressources informatiques et de communiquer efficacement.

Cependant, un réseau plat dans lequel tous les équipements appartiennent au même segment présente plusieurs limites :

- Absence d'isolation entre les différents départements.
- Propagation potentiellement importante du trafic de diffusion (Broadcast).
- Difficulté à appliquer des politiques de sécurité adaptées.
- Dépendance à certains équipements réseau.
- Risque d'interruption des communications en cas de panne.
- Difficulté d'administration et d'évolution de l'infrastructure.

**Problématique :**

Comment concevoir une infrastructure réseau d'entreprise structurée, sécurisée et évolutive, permettant d'isoler les différents départements tout en assurant la disponibilité et la continuité des communications ?

## 🎯 2. Objectifs du projet

Le projet poursuit les objectifs suivants :

### Architecture réseau
- Concevoir une architecture réseau hiérarchique.
- Organiser les équipements selon les différentes couches du réseau.
- Structurer les connexions entre les équipements d'accès, de distribution et de cœur de réseau.

### Segmentation
- Créer des VLAN pour séparer logiquement les départements.
- Définir des sous-réseaux IP adaptés aux différents segments.
- Mettre en place le routage inter-VLAN pour permettre les communications autorisées.

### Sécurité
- Isoler les différents départements.
- Contrôler les communications entre les VLAN.
- Appliquer des mécanismes de filtrage du trafic.
- Sécuriser les accès aux équipements réseau.

### Haute disponibilité
- Introduire des mécanismes de redondance.
- Réduire les points uniques de défaillance (Single Point of Failure).
- Prévoir des mécanismes permettant de maintenir les communications en cas de défaillance d'un équipement ou d'un lien.

### Validation
- Tester la connectivité entre les différents équipements.
- Vérifier l'isolation des VLAN.
- Contrôler les communications inter-départements.
- Vérifier le comportement de l'infrastructure lors des scénarios de panne.

## 🏗️ 3. Architecture réseau

Le réseau repose sur une architecture hiérarchique organisée autour de trois couches :

| Couche | Rôle |
|---|---|
| Core Layer | Assurer le transport rapide du trafic entre les différentes parties du réseau. |
| Distribution Layer | Agréger les connexions, appliquer les politiques réseau et assurer le routage. |
| Access Layer | Connecter les équipements terminaux : ordinateurs, imprimantes et autres périphériques. |

Cette organisation facilite l'administration, améliore la modularité et permet de faire évoluer l'infrastructure.

### Vue de l'architecture
<img width="816" height="603" alt="image" src="https://github.com/user-attachments/assets/1fcaffa6-ea17-41ef-b86d-cf853efdd512" />


## 🧩 4. Technologies et fonctionnalités

Les technologies et mécanismes étudiés dans ce projet comprennent :

| Technologie | Fonction |
|---|---|
| Cisco Packet Tracer | Conception et simulation de l'infrastructure réseau. |
| VLAN | Segmentation logique du réseau. |
| IEEE 802.1Q | Transport des VLAN sur les liens trunk. |
| Routage inter-VLAN | Communication entre les différents réseaux locaux. |
| Adressage IPv4 | Identification et organisation des équipements. |
| ACL | Contrôle et filtrage des communications réseau. |
| STP | Prévention des boucles de niveau 2. |
| Redondance réseau | Amélioration de la disponibilité de l'infrastructure. |

*Les mécanismes effectivement configurés doivent être confirmés à partir de la topologie et des configurations du projet.*

## 🔐 5. Segmentation et sécurité

La segmentation logique permet de séparer les départements de l'entreprise au moyen de VLAN distincts.

Chaque département dispose ainsi de son propre domaine de broadcast et de son propre plan d'adressage IP.

Cette organisation permet notamment :

- De limiter les communications non nécessaires entre départements.
- De réduire les domaines de broadcast.
- De faciliter l'administration du réseau.
- D'appliquer des règles de sécurité spécifiques.
- De mieux maîtriser les flux de communication.

Les ACL peuvent notamment être utilisées pour autoriser ou refuser certains flux entre les différents sous-réseaux.

## 🔄 6. Redondance et disponibilité

La disponibilité constitue un élément essentiel de l'infrastructure.

Une défaillance d'un équipement réseau ou d'un lien ne devrait pas provoquer une interruption générale des communications.

L'architecture prévoit donc l'étude de mécanismes de redondance permettant de limiter les conséquences de telles défaillances.

Parmi les mécanismes concernés :

- Redondance des équipements réseau.
- Redondance des liens de communication.
- Spanning Tree Protocol (STP) pour gérer les chemins redondants de niveau 2.
- Mécanismes de passerelle redondante lorsque cela est nécessaire.

L'objectif est d'améliorer la résilience de l'infrastructure et de limiter les interruptions de service.

## 🧪 7. Tests et validation

La validation de l'infrastructure repose sur plusieurs scénarios de test.

| Test | Résultat attendu |
|---|---|
| Connectivité au sein d'un même VLAN | Communication fonctionnelle. |
| Communication inter-VLAN autorisée | Communication fonctionnelle selon les règles définies. |
| Communication inter-VLAN interdite | Trafic bloqué conformément aux ACL. |
| Attribution des adresses IP | Configuration IP conforme au plan d'adressage. |
| Vérification des liens trunk | Transport des VLAN autorisés. |
| Vérification STP | Absence de boucle de niveau 2. |
| Défaillance d'un lien redondant | Maintien de la connectivité si un chemin alternatif est disponible. |
| Défaillance d'un équipement redondé | Basculement si le mécanisme de redondance configuré le permet. |

Les tests sont effectués dans Cisco Packet Tracer à l'aide des commandes réseau et des outils de simulation.

## 🛠️ 8. Outils utilisés

- **Cisco Packet Tracer** : conception, configuration et simulation du réseau.
- **Cisco IOS CLI** : configuration des équipements Cisco.
- **Git et GitHub** : versionnement et documentation du projet.

## 📂 9. Structure du dépôt

```text
Projet_CISCO/
│
├── Projet_réseau_packet_tracer.docx
│   └── Document de présentation du projet
│
├── README.md
│   └── Documentation du projet
│
└── [Fichiers de simulation à ajouter]
    └── Topologie Cisco Packet Tracer (.pkt)
```

## 🚀 10. Installation et utilisation

### Prérequis

- Un ordinateur sous Windows, Linux ou macOS.
- Cisco Packet Tracer installé.
- Le fichier de simulation du projet au format `.pkt` (lorsqu'il est disponible).

### Récupération du projet

```bash
git clone https://github.com/kossibihaho/Projet_CISCO.git
```

Accéder au répertoire :

```bash
cd Projet_CISCO
```

### Lancement de la simulation

1. Ouvrir Cisco Packet Tracer.
2. Charger le fichier de simulation `.pkt`.
3. Examiner la topologie réseau.
4. Accéder aux équipements Cisco.
5. Vérifier les configurations.
6. Exécuter les différents scénarios de test.

## 📚 11. Compétences développées

Ce projet permet de mettre en pratique plusieurs compétences en réseaux et systèmes :

- Conception d'architectures réseau d'entreprise.
- Compréhension des architectures hiérarchiques.
- Segmentation réseau avec les VLAN.
- Configuration des équipements Cisco.
- Routage et communication inter-VLAN.
- Mise en œuvre de politiques de filtrage avec les ACL.
- Compréhension des mécanismes de redondance.
- Diagnostic et résolution des problèmes réseau.
- Simulation et validation d'infrastructures informatiques.

## 👨‍💻 12. Auteur

**Kossi BIHAHO**

Étudiant en informatique, orienté Réseaux, Systèmes et Cloud Computing.

- GitHub : [@kossibihaho](https://github.com/kossibihaho)
- LinkedIn : [Kossi BIHAHO](https://www.linkedin.com/in/kossi-bihaho-0624a6363/)

## 📄 13. Licence

Ce projet est réalisé dans un cadre académique.

Toute réutilisation ou adaptation du contenu doit mentionner le dépôt original.

---

⭐ Si ce projet vous intéresse, n'hésitez pas à consulter le dépôt et à suivre son évolution.
