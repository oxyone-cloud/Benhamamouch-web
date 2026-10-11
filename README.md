<p align="center">
  <img width="640" alt="OxyONE Cloud Ecosystem" src="https://github.com/user-attachments/assets/8f1fa2cb-4784-42d7-afd8-2e8b0cfc6217" />
</p>

<p align="center">
  <a href="https://orcid.org/0009-0000-1250-8205">
    <img src="https://img.shields.io/badge/ORCID-0009--0000--1250--8205-A6CE39?style=flat&logo=orcid&logoColor=white" alt="ORCID"/>
  </a>
  <img src="https://img.shields.io/badge/Startup_Labellisée-Algérie-blue?style=flat&logo=rocket&logoColor=white" alt="Startup Labellisée"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white" alt="Google Cloud"/>
  <img src="https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase" alt="Firebase"/>
  <img src="https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white" alt="Flutter"/>
  <img src="https://img.shields.io/badge/Cloud-Architecture-orange?style=for-the-badge&logo=cloud&logoColor=white" alt="Cloud"/>
  <img src="https://img.shields.io/badge/Logistics-IoT-informational?style=for-the-badge&logo=logistics&logoColor=white" alt="Logistique"/>
</p>

# 🚀 OxyONE / SSCI Cloud Ecosystem

Plateforme Cloud & IoT pour la gestion, la traçabilité et le suivi de la chaîne du froid en temps réel (Application Cloud-SaaS, Flutter, Firebase & GCP Cloud Run).

---

## 🌐 Liens Principaux
* **Portail Web (Production) :** [https://oxyone-portal-cb9aa.web.app/](https://oxyone-portal-cb9aa.web.app/)
* **Dépôt GitHub Web :** [https://github.com/oxyone-cloud/Benhamamouch-web](https://github.com/oxyone-cloud/Benhamamouch-web)

---

## 🏗️ Architecture Globale

```mermaid
flowchart TD
    subgraph FRONTEND ["📱 Front-End Applications (Flutter / Web / Mobile)"]
        A1["❄️ OxyONE App"]
        A2["🧊 Cold Storage App"]
        A3["📡 Smart Tracking System"]
    end

    subgraph CLOUD_INFRA ["☁️ Google Cloud & Firebase Infrastructure"]
        B1["🔥 Firebase Hosting\n(oxyone-portal-cb9aa.web.app)"]
        B2["🔐 Firebase Auth"]
        B3["📊 Cloud Firestore\n(Données Télémétriques IoT)"]
        B4["⚡ Cloud Functions\n(Digital Sense Core)"]
        B5["🐳 GCP Cloud Run\n(Backend SSCI APIs)"]
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
