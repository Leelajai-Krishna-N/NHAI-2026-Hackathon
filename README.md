# ReflectAI — NHAI 6th Innovation Hackathon Submission

**Team:** Powerhouse  
**Hackathon:** NHAI 6th Innovation Hackathon  
**Problem Statement:** Retroreflectivity Measurement of Road Signs, Pavement Markings & Road Studs  
**Approach:** Option iii — Vehicle-Mounted Sensor Fusion + AI/ML/Computer Vision  

---

## 💡 Our Idea

India's national highways have millions of retroreflective assets — traffic signs, pavement markings, road studs, and delineators — all of which degrade over time and must meet IRC 67/IRC 35 standards to ensure nighttime and low-visibility safety. The current method of manual, handheld retroreflectometer measurement is dangerously slow, exposes inspection crews to live high-speed traffic, and covers only a tiny fraction of the network at any given time.

**ReflectAI** is an AI-powered retroreflectivity intelligence platform that solves this at scale.

A survey vehicle equipped with a calibrated NIR-LED illumination bar, stereo HDR cameras, RTK-GPS, and an edge AI processor travels the highway at normal operating speed (60–100 km/h). On board, a YOLOv9-based detector identifies every retroreflective asset in real time, while a dual-path estimation engine — combining a physical photometric model with a deep learning regression network — computes absolute RL values in mcd/m²/lux for each asset, geo-tagged to sub-metre accuracy.

The results feed into a cloud intelligence engine that predicts degradation up to 18 months ahead, prioritizes maintenance, and surfaces everything through a GIS-based dashboard with contractor work order workflows.

### Key Highlights

- **100% continuous coverage** at highway speed — no lane closures, no crew on live road
- **Dual-path RL estimation** — physical model + CNN regression cross-validate each other for self-healing data quality
- **All-weather operation** — 6 condition-specific model variants (dry/wet × day/night/fog), built for Indian monsoon conditions
- **Predictive degradation engine** — 18-month RL forecast per asset using Random Forest ensemble (R² = 0.97 in literature)
- **Multi-asset in one pass** — pavement markings, road studs, shoulder signs, and gantry signs (via drone module)
- **End-to-end platform** — from sensor to GIS heatmap to maintenance work order

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `PowerhouseNHAIHackathon.docx` | Full concept note and architecture document — includes system overview, 5-layer architecture, AI/ML pipeline, data flow, innovation highlights, feasibility analysis, scalability plan, and competitive differentiation |
| `PowerhouseNHAIHackathon.pdf` | PDF version of the same concept note and architecture document, formatted for easy review |
| `PowerhouseNHAIHackathon.rar` | Archive containing all submission files |

---

## 🏗️ System Architecture

| Layer | Description |
|------|------------|
| **Layer 1 — Data Acquisition** | Stereo HDR Camera + NIR LED + RTK-GPS + Weather Sensors |
| **Layer 2 — Edge Computing** | NVIDIA Jetson Orin — real-time detection & RL estimation |
| **Layer 3 — AI/ML Engine** | Degradation prediction, anomaly detection, prioritization |
| **Layer 4 — Data Platform** | Time-series DB, GIS integration, REST APIs, IRC reports |
| **Layer 5 — Dashboard** | Web + mobile interface with heatmaps & workflows |

---

## 📬 Contact

For queries related to this submission, please refer to the NHAI Hackathon portal:  
🌐 [https://hackathon.nhai.org/Hackathon/](https://hackathon.nhai.org/Hackathon/)
