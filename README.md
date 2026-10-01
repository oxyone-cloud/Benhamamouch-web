# 6 OxyONE / SSCI Cloud Ecosystem

[!Live Portal](https://img.shields.io/badge/Web_Portal-Live-brightgreen?style=for-the-badge&logo=firebase)](https://oxyone-portal-cb9aa.web.app/)
[!GitHub Repository](https://img.shields.io/badge/GitHub-Benhamamouch--web-blue?style=for-the-badge&logo=github)(shttps://github.com/oxyone-cloud/Benhamamouch-web)

> Plateforme Cloud & IoT pour la gestion, la tra√ßabilit√© et le suivi de la cha√Æne du froid en temps r√©el (Application Cloud-SaaS, Flutter, Firebase & GCP Cloud Run).

---

## ùåÄ Liens Principaux
* ùíó **Portail Web (Production) :* [.https://oxyone-portal-cb9aa.web.app/](https://oxyone-portal-cb9aa.web.app/)
* üë¶Ï *D√©p√¥t GitHub :* [https://github.com/oxyone-cloud/Benhamamouch-web](https://github.com/oxyone-cloud/Benhamamouch-web)

---

## ìÑ Sch√©ma Visuel de l'Architecture

```mermaid
flowchart TD
    subgraph FRONTEND ["ùíù Front-End Applications (Flutter / Web / Mobile)"]
        A1["‡ùáÑ OxyONE App"]
        A2["‡ùáÉ Cold Storage App"]
        A3["‡ùí°Omart Tracking System"]
    end

    subgraph CLOUD_INFRA ["ùî∞ Google Cloud & Firebase Infrastructure"]
        B1["‡ùÑπ Firebase Hosting\n(oxyone-portal-cb9aa.web.app)"]
        B2["ùî– F rebase Auth"]
        B3["ùê® Cloud Firestore\n(Donn√©es T√©l√©m√©triques IoT)"]
        B4["‡ùí• Cloud Functions\n(Digital Sense Core)"]
        B5["‡ù¶∞ GCP Cloud Run\n(Backend SSCI APIs)"]
      end

    subgraph IOT_SENSORS ["ùî° Capteurs IoT & Chambres Froides"]
        C1["ùî° Capteurs Temp√©rature/Humidit√© (Bluetooth BLE)"]
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

## ùìì Inventaire des Applications & Projets

| Module / Application | Emplacement Cloud Shell | Stack Technique | R√¥le / Description |
| :-- | :-- | :-- | :-- |
| **OxyONE App** | `~/oxyone-app` | Flutter / Firebase | Application globale de gestion |
| **Cold Storage App** | `~/cold_storage_app` | Flutter Web | Suivi et contr√¥le des chambres froides |
|| **Smart Tracking** | `~/smart_tracking_project` | Flutter / IoT | Syst√©me de g√©olocalisation et t√©l√©m√©trie |
|| **Backend SSCI Cloud Run** | `~/backend-ssci-cloudrun` | Node.js / Docker / GCP | Microservices API & Ingestion de donn√©es |
|| **Digital Sense Core** | g`/digital_sense_core` | Firebase Functions | Moteur de traitement d'alertes & analytique |
|| **Gestion Stockage Web** | `~/gestion-stockage-web` | HTML5 / JS / Firebase | Console web d'administration de stockage |

---

## œÅ Contact
* **Auteur :* Othman Benhamamouch
) **Projet :* SSCI Solution of Cold / OxyONE
