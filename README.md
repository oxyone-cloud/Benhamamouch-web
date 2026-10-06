[![ORCID](https://img.shields.io/badge/ORCID-0009--0000--1250--8205-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0000-1250-8205)

# 🚀 OxyONE / SSCI Cloud Ecosystem

[![Live Portal](https://img.shields.io/badge/Web_Portal-Live-brightgreen?style=for-the-badge&logo=firebase)](https://oxyone-portal-cb9aa.web.app/)
[![GitHub Repository](https://img.shields.io/badge/GitHub-Benhamamouch--web-blue?style=for-the-badge&logo=github)](https://github.com/oxyone-cloud/Benhamamouch-web)

> Plateforme Cloud & IoT pour la gestion, la traçabilité et le suivi de la chaîne du froid en temps réel (Application Cloud-SaaS, Flutter, Firebase & GCP Cloud Run).
🌐 Liens Principaux
🔗 Portail Web (Production) : https://oxyone-portal-cb9aa.web.app/

📦 Dépôt GitHub : https://github.com/oxyone-cloud/Benhamamouch-web
flowchart TD
    subgraph FRONTEND ["📱 Front-End Applications (Flutter / Web / Mobile)"]
        A1["❄️ OxyONE App"]
        A2["🧊 Cold Storage App"]
        A3["📡 Smart Tracking System"]
    end

    subgraph CLOUD_INFRA ["☁️ Google Cloud & Firebase Infrastructure"]
        B1["🔥 Firebase Hosting
(oxyone-portal-cb9aa.web.app)"]
        B2["🔐 Firebase Auth"]
        B3["📊 Cloud Firestore
(Données Télémétriques IoT)"]
        B4["⚡ Cloud Functions
(Digital Sense Core)"]
        B5["🐳 GCP Cloud Run
(Backend SSCI APIs)"]
    end

    subgraph IOT_SENSORS ["📟 Capteurs IoT & Chambres Froides"]
        C1["🌡️ Capteurs Température/Humidité (Bluetooth BLE)"]
    end

    C1 -->|Sync Bluetooth / Telemetry| A2
    C1 -->|Sync Bluetooth / Telemetry| A3
    A1 & A2 & A3 -->|HTTPS / gRPC| B1
    A1 & A2 & A3 -->|Realtime Sync| B3
    B1 --> B2
    B3 --> B4
    B4 --> B5
   ## 📂 Inventaire des Applications & Projets

| Module / Application | Emplacement Cloud Shell | Stack Technique | Rôle / Description |
| :--- | :--- | :--- | :--- |
| **OxyONE App** | `~/oxyone-app` | Flutter / Firebase | Application globale de gestion |
| **Cold Storage App** | `~/cold_storage_app` | Flutter Web | Suivi et contrôle des chambres froides |
| **Smart Tracking** | `~/smart_tracking_project` | Flutter / IoT | Système de géolocalisation et télémétrie |
| **Backend SSCI Cloud Run** | `~/backend-ssci-cloudrun` | Node.js / Docker / GCP | Microservices API & Ingestion de données |
| **Digital Sense Core** | `~/digital_sense_core` | Firebase Functions | Moteur de traitement d'alertes & analytique |
| **Gestion Stockage Web** | `~/gestion-stockage-web` | HTML5 / JS / Firebase | Console web d'administration de stockage |
    ⚙️ Back-End & Services Cloud
Google Cloud Platform (GCP) : Cloud Run (Microservices conteneurisés Docker), Cloud Shell, BigQuery.

Firebase Services : Authentication, Cloud Firestore (Base NoSQL temps réel), Cloud Functions, Hosting (oxyone-portal-cb9aa.web.app).

📄 Informations & Contact
Auteur : Othman Benhamamouch

Projet : SSCI Solution of Cold / OxyONE


## Déploiement GCP
Projet géré sur Google Cloud Shell ().
