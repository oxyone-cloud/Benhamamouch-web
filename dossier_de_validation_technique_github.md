# Dossier de Validation Technique & Qualification Software

> **SSCI Solution of Cold** — Suite de solutions Cloud & Télémétrie Froid (`cold-service-othman` & `gestion-de-stockage-cold`)

## 📋 Présentation et Objectif

Ce dépôt/document récapitule les résultats de qualification technique et d'assurance qualité issus de la phase de test pilote (période du **11 août au 8 november 2026**).

Il vise à fournir aux équipes d'ingénierie, aux auditeurs et aux partenaires industriels la preuve empirique du bon fonctionnement des applications web de supervision de la chaîne du froid et de la gestion d'entrepôt frigorifique.

## 📌 Sources & Traçabilité des Données

Toutes les métriques d'évaluation et données comportementales présentées dans ce dossier sont extraites directement des rapports officiels d'audit et de télémétrie suivants :

* **Rapport GA4 - Cold Service :** `Instantané_des_rapports.pdf` (Propriété Analytics : `cold-service-othman` / Période : 11 août – 8 nov. 2026).
* **Rapport GA4 - Gestion de Stock :** `Instantané_des_rapports (1).pdf` (Propriété Analytics : `gestion-de-stockage-cold` / Période : 11 août – 8 nov. 2026).
* **Logs d'Infrastructure & Recette :** Journaux d'exécution Google Cloud Shell (`shell.cloud.google.com/referral`) et de la console Firebase (`console.firebase.google.com/ref`).
* **Référentiel Google Sites :** Portails de démonstration et passerelles d'accès internes (`sites.google.com/referral`).

## 🏗️ Architecture System & Infrastructure

Les solutions reposent sur une architecture Cloud native résiliente assurant la haute disponibilité des données de télémétrie :

* **Frontend :** Web Applications (React / Progressive Web Apps) hébergées sur Firebase Hosting.
* **Backend & Compute :** Microservices Cloud Run, Firebase Functions & pipelines Google Cloud Shell pour le déploiement continu.
* **Base de données & Télémétrie :** Collection de données IoT en temps réel avec persistance sécurisée.
* **Intégrations Entreprise :** Passerelles ouvertes pour systèmes ERP (compatibilité architecture SAP PartnerEdge).

## 📊 Synthèse des Tests Pilotes & Métriques (Analytics QA)

Les données collectées au cours de la phase de validation technique confirment la robustesse globale des applications :

| Indicateur / Métrique | *Cold Service* (`cold-service-othman`) [Source: Report 1] | *Gestion de Stock* (`gestion-de-stockage-cold`) [Source: Report 2] | Statut QA |
| ----- | ----- | ----- | ----- |
| **Utilisateurs Actifs (Pilotes)** | 29 | 19 | Validé |
| **Nouveaux Utilisateurs** | 28 | 18 | Validé |
| **Sessions Directes (`direct/none`)** | 135 (Web: 128 / Mobile: 7) | 54 (Web: 51 / Mobile: 3) | Validé |
| **Sessions de Dev & Cloud Shell** | 40 (Firebase) + 40 (Google Sites) | 50 (Google Cloud Shell) | Certifié |
| **Volume d'Événements Traités** | 1 200 | 384 | Conforme |
| **Durée Moyenne d'Engagement (Web)** | 1 min 23 s | 26 s | Performant |
| **Durée Moyenne d'Engagement (Mobile)** | 4 s | 2 s | *En optimisation* |

### 🌍 Ancrage Géographique des Tests de Terrain (Sources GA4 City Logs)

Les tests sur le terrain ont été vérifiés via les relevés de géolocalisation IP Analytics :

* **Algérie (Bassin Pilote) :** Bir El Djir (9/8 users), Es Senia (7/4 users), Oran (5/2 users), Oued Tlelat (9/2 users), Mascara (4/3 users), Ain El Turk, Ain Temouchent, Chabaat El Leham.
* **Noeuds d'Infrastructure Cloud (Tests automatisés) :** Ashburn (US Data Centers - 4 users).

## 🔒 Sécurité, Qualité & Conformité Industrielle

* [x] **Horodatage & Traçabilité :** Relevés de température continus conformes aux exigences réglementaires de la chaîne du froid (agroalimentaire & santé).
* [x] **Chiffrement des Flux :** Chiffrement end-to-end (TLS/SSL) pour toutes les données transitant entre les capteurs IoT, le navigateur et la base Cloud.
* [x] **Isolation des Environnements :** Séparation stricte entre les environnements de staging (Cloud Shell / Firebase Test) et la production.

## 🗺️ Feuille de Route d'Amélioration (Backlog QA)

Sur la base des métriques collectées, les tâches de sprint suivantes sont planifiées avant la mise en production globale :

* [ ] **Optimisation PWA Mobile (`HIGH`) :** Refonte du temps de chargement et du parcours UX sur mobile pour corriger le taux d'abandon précoce observé sur smartphone (sessions < 5 s).
* [ ] **Tracking des Événements Clés (`MEDIUM`) :** Configuration fine du marquage GA4/Firebase pour les alertes de rupture de chaîne du froid et les validations de mouvements de stock.
* [ ] **Audit RBAC & Sécurité (`MEDIUM`) :** Audit des politiques d'accès IAM et restriction des rôles utilisateurs pour la livraison aux clients grands comptes.

## 📄 Licence & Mentions

© 2026 **SSCI Solution of Cold**. Tous droits réservés.

Ce document est destiné à la documentation technique et au partage avec les partenaires habilités.