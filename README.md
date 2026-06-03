# DxCortex — AI-Powered Radiology Reporting SaaS

> Automated DICOM report generation for radiology clinics using Claude AI — cutting report turnaround from **4 hours to 20 minutes**.

---

## The Problem

Radiology clinics were spending 4+ hours per day manually transcribing DICOM scan data into reports. Radiologists had to switch between PACS software and reporting tools, copy-paste patient data, and format reports by hand — leading to errors, delays, and burnout.

---

## The Solution

DxCortex is a multi-tenant SaaS platform that integrates directly with clinic PACS systems (Orthanc, GE Voluson S8) via the DICOM protocol. It automatically extracts scan metadata, sends it to Claude AI for report drafting, and delivers a formatted report — ready for radiologist review in under 20 minutes.

**Architecture:**
```
GE Voluson S8 → DICOM Protocol → Orthanc PACS → Python Flask API
→ AWS S3 (scan storage) → Claude API (report generation)
→ n8n (workflow orchestration) → Clinic Dashboard (report delivery)
```

---

## Results

| Metric | Before | After |
|---|---|---|
| Report turnaround | 4 hours | 20 minutes |
| Manual transcription errors | Frequent | Zero |
| Clinics served | — | 3 (multi-tenant) |
| System uptime | — | 99.5% |

---

## Tech Stack

| Layer | Tools |
|---|---|
| Workflow Orchestration | n8n |
| AI Report Generation | Claude API (Anthropic) |
| DICOM Integration | Orthanc PACS, GE Voluson S8 |
| Backend API | Python Flask |
| OCR | Google Vision API |
| Storage | AWS S3 |
| Deployment | AWS EC2, Docker |
| Auth (Multi-tenant) | Firebase Authentication |

---

## Key Features

- **DICOM Integration** — Direct connection with Orthanc PACS via DICOM protocol
- **AI Report Drafting** — Claude API generates structured radiology reports from scan metadata
- **Multi-tenant** — 3 independent clinic instances on one platform
- **OCR Pipeline** — Extracts text from scanned documents using Google Vision API
- **Automated Billing Workflows** — n8n handles invoice generation and delivery
- **Radiologist Review Dashboard** — Clean UI for report review and approval before sending to patients

---

## Impact

> *"Report turnaround dropped from 4 hours to under 20 minutes. Our radiologists now spend time reviewing, not typing."*

- 3 radiology clinics running in production
- Zero manual transcription errors since deployment
- 99.5% uptime on AWS EC2 + Docker infrastructure

---

## Built By

**Krishan Kumar** — AI Automation Engineer | n8n Developer | LangChain | Python  
📧 kk88987@gmail.com | 📍 Ghaziabad, India | Open to Remote

> Interested in a similar system for your clinic or healthcare business? Reach out.
