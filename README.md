# Zenith OS — Zero-Capex Industry 4.0 Optical Operating System

> **BUILD 2036 | Frontier 04: Manufacturing Renaissance (Industry 4.0 & Next-Gen Supply Chains)**  
> Transforming any existing ONVIF/RTSP industrial IP camera into an autonomous, Zero-Trust smart factory and supply-chain command plane—without replacing a single camera.

[![Live Prototype](https://img.shields.io/badge/Live%20Prototype-Google%20Cloud%20Run-15803D?style=for-the-badge)](https://zenith-os-dashboard-610496103443.asia-south1.run.app)
[![Demo Video](https://img.shields.io/badge/Demo%20Video-3%20Min%20Walkthrough-D91E2A?style=for-the-badge)](INSERT_DEMO_VIDEO_URL)
[![License](https://img.shields.io/badge/License-All%20Rights%20Reserved-0F172A?style=for-the-badge)](#license)

---

## ⚡ 30-Second Evaluator Verification Playbook

Verify the live deployment directly in any desktop browser (no installation required):

1. **Live Plant Command Deck (`PLANT_SEC`):**  
   Open **[zenith-os-dashboard](https://zenith-os-dashboard-610496103443.asia-south1.run.app)** → click **Authenticate** (pre-filled PIN: `SEC-2026`) → launch **SIPCOT Plant 01** → verify the live 2×2 watermarked feed matrix, **99.99% bandwidth saved** telemetry, Bay F28 Dock SLA timer, and live hazard intercepts.
2. **Executive Zero-Trust Lockout (`HQ_EXEC`):**  
   Click **SIGN OUT** (top-right) → select **HQ Executive** (PIN: `HQ-2026`) → confirm raw site LAN feeds are locked while group-wide GIS KPIs, Dock SLA ledgers, 10-min AMC tickets, on-demand DPDP-redacted clips, and `SECURITY & AUDIT` remain live.
3. **Edge Reverse-Proxy 403 Proof:**  
   Open **[Edge Stream Endpoint](https://34.100.220.25.sslip.io/cam01/zenith_feed)** directly without a signed token → confirm `403 Forbidden: Valid Zenith OS Stream Token Required`.

---

## 🏭 The Industrial Problem

Multi-plant manufacturing groups operate hundreds of standard ₹3k–₹5k IP cameras across mixed-vendor estates that remain operationally blind—leaking crores annually to loading-bay detention penalties, shop-floor fire/PPE delays, and unnoticed camera downtime.

* **Rip-and-Replace Fails:** Upgrading 30–200 cameras to standalone cloud-AI hardware costs **₹37L–₹40L+ per plant** and saturates factory WAN bandwidth.
* **Legacy NVRs Lose Evidence:** Local NVRs run siloed per plant and overwrite footage every **15–30 days**, leaving teams blind during audits, disputes, and insurance claims.

## 🚀 The Zenith OS Solution

Zenith OS is **100% hardware-agnostic**. It plugs a compact on-premise edge node (**NVIDIA Jetson Orin Nano 8GB** for zero-Capex pilots; **NVIDIA RTX Edge Server** for 20–30 camera plants) directly into existing ONVIF/RTSP IP cameras and NVRs:

1. **99.99% Local Edge Filtering:** Local `YOLOv8n` + OpenCV Laplacian blur gating (`σ² ≥ 35`) filters raw video on-site at ₹0 API cost and redacts worker faces for DPDP compliance. **Zero raw video leaves the factory LAN.**
2. **Multimodal Industrial Reasoning:** Only sharp, verified event frames route over outbound HTTPS to **Vertex AI (Gemini 2.5 Flash)** for contextual operational reasoning at **~₹0.07 (7 paise) per event**.
3. **Multi-Year Incident Vault & Group-Wide GIS:** By archiving only verified event crops and 1–2 minute incident clips, Zenith OS retains **years of searchable audit evidence** (eliminating 15–30 day NVR overwrites) unified across every manufacturing unit in one GIS command deck.

---

## 🧩 Core Industrial Modules (Frontier 04)

| Module | Camera / Scope | Frontier 04 Pillar | Operational Output |
| :--- | :--- | :--- | :--- |
| **Gate ANPR & Fleet Watchlist** | `CAM01` | Next-Gen Supply Chain | Zero-shot plate & vehicle classification; flagged-plate watchlist syncs to all edge nodes in **~5 seconds**. |
| **Dock TAT & Detention SLA** | `CAM02` (Bay F28) | Next-Gen Supply Chain | Live truck dwell timer against a **45-min SLA**, worker/forklift counts, and automated detention alerts. |
| **DPDP-Compliant EHS & PPE** | `CAM03` | Smart Factory Intelligence | Detects missing hardhats/vests and unsafe machine posture while blurring faces on-edge before cloud transit. |
| **Fire & Hazard Triage** | `CAM04` | Predictive Safety | Instant `FIRE-CRITICAL` intercepts with audible control-room chimes, severity scoring, and suppression guidance. |
| **10-Min Camera AMC SLA** | `ALL CAMS` | Asset Uptime | 1-second heartbeat watchdog auto-opens vendor SLA tickets if any camera is offline >10 min and auto-resolves on recovery. |
| **Multi-Year Vault & Group GIS** | `ENTERPRISE` | Multi-Plant Scale | Semantic UDF search, SHA-256 chain-of-custody seals, 1-click CSV audit exports, and unified multi-unit GIS oversight. |

---

## 🏗️ Hybrid Edge-to-Cloud Architecture

```text
[Any Existing ONVIF / RTSP IP Camera & NVR] (Zero Camera Replacement)
                  │
                  ▼
┌──────────────────────────────────────────────────────────┐
│ ZONE 1: ON-PREM EDGE NODE (Jetson Orin Nano / RTX Node)  │
│ • YOLOv8n Local Detection + OpenCV Blur Gate (σ² ≥ 35)   │
│ • On-Edge DPDP Face Redaction + Local Clip Ring Buffer   │
│ • Caddy TLS 1.3 Reverse Proxy (HTTP 403 Token Lock)      │
└─────────────────┬────────────────────────────────────────┘
                  │  Outbound HTTPS Only (0 Open Inbound Ports)
                  │  0.01% Sharp Event Frames (99.99% BW Saved)
                  ▼
┌──────────────────────────────────────────────────────────┐
│ ZONE 2 & 3: CLOUD AI & REAL-TIME CUSTODY                 │
│ • Vertex AI (Gemini 2.5 Flash) → Structured JSON (~7p)   │
│ • Firebase RTDB → Sub-Second Alerts, SLA, SHA-256 Audits │
│ • Multi-Year Event Vault → Crops + 1–2 Min Event Clips   │
└─────────────────┬────────────────────────────────────────┘
                  │
                  ▼
┌──────────────────────────────────────────────────────────┐
│ ZONE 4: ZERO-TRUST COMMAND PLANE (Google Cloud Run)      │
│ • React 18 + Vite + Tailwind + React-Leaflet Group GIS   │
│ • Role-Based Access Gate (PLANT_SEC / EHS / HQ_EXEC)     │
│ • Dynamic Diagonal Forensic Watermark + CSV Audit Export │
└──────────────────────────────────────────────────────────┘
```

---

## 📊 Measured Benchmarks & Unit Economics

| Metric | Legacy NVR / Cloud VMS | **Zenith OS (Measured)** |
| :--- | :--- | :--- |
| **Cloud Bandwidth Egress** | 4–8 Mbps/cam continuous | **99.99% Reduction** (`27,484.6 MB → 1,843.8 KB`) |
| **AI Reasoning Cost** | Unviable 24×7 cloud upload | **~₹0.07 / verified event** (Gemini 2.5 Flash) |
| **Year-1 Cost (30-Cam Plant)** | ₹12.8L – ₹38.9L+ (Rhombus / Verkada) | **₹1.8L – ₹2.3L** (**85%–94% lower**) |
| **Evidence Retention** | 15–30 days (rolling overwrite) | **Multi-Year Archival** (crops + 1–2 min clips) |
| **Stream Scraping Defense** | Open RTSP / VPN exposure | **100% Blocked** (`HTTP 403` at Caddy proxy) |
| **Watchlist Edge Sync** | Manual per-site update | **~5 seconds** across all edge nodes |

---

## 🔐 3-Layer Zero-Trust Security

1. **Access Control & Signed Edge Streams:** Role-based gateway (`PLANT_SEC`, `EHS_OFFICER`, `HQ_EXEC`) isolates raw feeds from executives; Caddy TLS 1.3 enforces signed stream tokens (`403 Forbidden` on direct scraping) with zero open inbound plant firewall ports.
2. **Anti-Leak & Data Residency:** Dynamic diagonal forensic watermarking (`email · role · camera ID · live UTC`) deters screen recording; on-edge DPDP face redaction ensures raw video never leaves the plant.
3. **Chain of Custody & Immutable Auditability:** Every evidence record is sealed with a **SHA-256 hash** and every login, role switch, clip pull, and export is logged to `/zenith_os/audit_logs` with 1-click CSV export.

---

## 📂 Repository Scope

This public showcase repository contains the **Zenith OS Command Deck frontend**, architecture documentation, and sanitized edge-pipeline reference scripts for BUILD 2036 evaluation. Proprietary production VLM prompt templates, enterprise client configurations, and deployment credentials are intentionally excluded for security and IP hygiene.

---

## 👥 Team

* **Vignesh A** — Co-Founder (B.E., MIT Chennai | MBA, IIM Raipur) · Industrial Surveillance Domain & Enterprise Process/SLA Architecture
* **Anirudh MR** — Co-Founder (B.E., MIT Chennai) · Digital Analytics, Data Engineering & Enterprise Modeling

## License

Copyright © 2026 Zenith OS (Vignesh A & Anirudh MR). **All Rights Reserved.**  
Provided strictly for **BUILD 2036 (Frontier 04)** hackathon evaluation. Unauthorized copying, commercial use, or redistribution is prohibited.
