# 🌌 Aura — AI-Powered Air Quality Operating System

**Aura** is an AI-powered operating system for air quality management, developed for the **Clear Skies Challenge 2025**.  
Our platform goes beyond monitoring — enabling city administrators and citizens to **predict, pinpoint, and proactively mitigate** air pollution.

---

## 📖 Table of Contents
- [Problem Statement](#-problem-statement)
- [Our Solution](#-our-solution)
- [Core Features](#-core-features)
- [System Architecture](#-system-architecture)
- [Technology Stack](#-technology-stack)
- [Project Status](#-project-status)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Roadmap](#-roadmap)
- [License](#license)

---

## 🎯 Problem Statement
Urban air quality management is stuck in a **reactive cycle**:  
Sparse, delayed data → guesswork policies → preventable public health crises.  

City authorities **lack predictive, high-resolution tools** for proactive governance — leading to slow and ineffective responses.

---

## ✨ Our Solution
**Aura** breaks this cycle by offering an **end-to-end AI platform** that ingests **multi-source data** and delivers **actionable insights**.  

Our first pilot city is **Gurugram, India**, one of the most challenging air quality environments in the world.

---

## 🚀 Core Features
Aura is powered by **three integrated engines**:

1. **🛰 The Sentinel Engine**  
   - AI model fusing satellite, ground, and weather data  
   - Generates **hyper-local** (100m) air quality maps  
   - Provides **48-hour forecasts**

2. **🕵 The Detective Engine**  
   - AI-driven **reverse atmospheric dispersion modeling**  
   - Traces pollution hotspots to probable sources  
   - Works in **near real-time**

3. **🧠 The Strategist Co-pilot**  
   - Generative AI policy sandbox  
   - Simulates environmental strategies instantly  
   - Example: *"What if we make this zone EV-only?"*

---

## 🏗️ System Architecture
Aura runs on a **scalable, cloud-native architecture**:

1. **Data Sources** → Ground stations, satellites, weather APIs  
2. **Data Fusion Engine** (Google Cloud) → Processing & storage in **BigQuery**  
3. **AI Models** → Sentinel, Detective, Strategist  
4. **APIs** → FastAPI backend  
5. **Frontend** → Interactive dashboards

![Aura System Architecture](link_to_your_architecture_diagram.png)

---

## 💻 Technology Stack
- **Backend**: Python, FastAPI  
- **Data Science & ML**: Pandas, GeoPandas, Scikit-learn, XGBoost, PyTorch (GNN)  
- **Cloud**: Google Cloud Platform (GCP)  
- **Storage**: Google Cloud Storage, BigQuery  
- **Compute & AI**: Vertex AI, Cloud Functions  
- **Geospatial**: Google Earth Engine API, QGIS/ArcGIS  
- **Frontend**: React, Deck.gl / Mapbox GL JS  
- **Generative AI**: Google Gemini Pro API  

---

## 📊 Project Status
**Current Phase**: **Milestone 1 — Predictive Model MVP ✅**  
Achievements:
- ✅ Cleaned & prepared Gurugram datasets  
- ✅ Fused **CPCB** ground station data with **MODIS AOD** satellite data  
- ✅ Baseline **XGBoost model** trained (R² = *0.82* on unseen test data)

**Next**: Milestone 2 — **Deep Learning model + Backend API**

---

## 🚀 Getting Started

### Prerequisites
- Python **3.9+**
- **Google Cloud SDK** installed & configured
- **Google Earth Engine** account

---

### Installation
```sh
# Clone the repository
git clone https://github.com/[your-username]/aura-project.git
cd aura-project

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Configure environment variables
cp .env.example .env
# Fill in your GCP credentials and API keys
