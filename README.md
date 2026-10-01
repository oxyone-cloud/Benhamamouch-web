#  OxyONE / SSCI Cloud Ecosystem

[!Live Portal](https://img.shields.io/badge/Web_Portal-Live-brightgreen?style=for-the-badge&logo=firebase)]
(https://oxyone-portal-cb9aa.web.app/)
[!GitHub Repository]
(https://img.shields.io/badge/GitHub-Benhamamouch--web-blue?style=for-the-badge&logo=github)(shttps://github.com/oxyone-cloud/Benhamamouch-web)

> Plateforme Cloud & IoT pour la gestion, la traÃ§abilitÃ© et le suivi de la chaÃ®ne du froid en temps rÃ©el (Application Cloud-SaaS, Flutter, Firebase & GCP Cloud Run).

---

 Liens Principaux
Portail Web (Production) :* [.https://oxyone-portal-cb9aa.web.app/](https://oxyone-portal-cb9aa.web.app/)
 GitHub :* [https://github.com/oxyone-cloud/Benhamamouch-web](https://github.com/oxyone-cloud/Benhamamouch-web)

---


 SchÃ©ma Visuel de l'Architecture

```mermaid
flowchart TD
    subgraph FRONTEND ["ð’ Front-End Applications (Flutter / Web / Mobile)"]
        A1["à‡„ OxyONE App"]
        A2["à‡ƒ Cold Storage App"]
        A3["à’¡Omart Tracking System"]
    end

    subgraph CLOUD_INFRA ["ð”° Google Cloud & Firebase Infrastructure"]
        B1[ Firebase Hosting\n(oxyone-portal-cb9aa.web.app)"]
        B2[F rebase Auth"]
        B3[Cloud Firestore\n(DonnÃ©es TÃ©lÃ©mÃ©triques IoT)"]
        B4[Cloud Functions\n(Digital Sense Core)"]
        B5[ GCP Cloud Run\n(Backend SSCI APIs)"]
      end

    subgraph IOT_SENSORS ["ð”¡ Capteurs IoT & Chambres Froides"]
        C1[¡ Capteurs TempÃ©rature/HumiditÃ© (Bluetooth BLE)"]
    end

    C1 -->|Sync Bluetooth / Telemetry| A2
    C1 -->|Sync Bluetooth / Telemetry| A3
    A1 & A2 & A3 -->|HTTPS / gRPC| B1
    A1 & A2 & A3 -->|Realtime Sync| B3
    B1 --> B2
    B3 --> B4
    B4 --> B5
```

---

Inventaire des Applications & Projets

| Module / Application | Emplacement Cloud Shell | Stack Technique | RÃ´le / Description |
| :-- | :-- | :-- | :-- |
| **OxyONE App** | `~/oxyone-app` | Flutter / Firebase | Application globale de gestion |
| **Cold Storage App** | `~/cold_storage_app` | Flutter Web | Suivi et contrÃ´le des chambres froides |
|| **Smart Tracking** | `~/smart_tracking_project` | Flutter / IoT | SystÃ©me de gÃ©olocalisation et tÃ©lÃ©mÃ©trie |
|| **Backend SSCI Cloud Run** | `~/backend-ssci-cloudrun` | Node.js / Docker / GCP | Microservices API & Ingestion de donnÃ©es |
|| **Digital Sense Core** | g`/digital_sense_core` | Firebase Functions | Moteur de traitement d'alertes & analytique |
|| **Gestion Stockage Web** | `~/gestion-stockage-web` | HTML5 / JS / Firebase | Console web d'administration de stockage |

---

## Ï Contact
* **Auteur :* Othman Benhamamouch
) **Projet :* SSCI Solution of Cold / OxyONE
