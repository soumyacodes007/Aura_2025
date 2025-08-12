Aura is an AI-powered operating system for air quality management, developed for the Clear Skies Challenge 2025. Our platform moves beyond simple monitoring to provide city administrators and citizens with the tools to predict, pinpoint, and proactively mitigate air pollution.
📖 Table of Contents
Problem Statement
Our Solution
Core Features
System Architecture
Technology Stack
Project Status
Getting Started
Prerequisites
Installation
Usage
Roadmap
Team
License
🎯 Problem Statement
Current urban air quality management is trapped in a vicious cycle: sparse, lagging data leads to reactive policies based on guesswork, ultimately resulting in a severe and preventable public health crisis. City authorities lack the predictive, high-resolution tools needed for proactive and effective environmental governance.
✨ Our Solution
Aura breaks this cycle. It's an end-to-end platform that ingests multi-source data to provide a clear, intelligent, and actionable view of a city's air quality. We empower decision-makers to move from reaction to prevention.
Our pilot city for this project is Gurugram, India, a region facing some of the world's most complex air quality challenges.
🚀 Core Features
Aura is built on three powerful, integrated modules:
The Sentinel Engine: A state-of-the-art AI model that fuses satellite, ground, and weather data to generate hyper-local (100m resolution) air quality maps and 48-hour forecasts.
The Detective Engine: An innovative source-attribution module that uses AI-driven reverse atmospheric dispersion modeling to trace pollution hotspots back to their most probable sources in near real-time.
The Strategist Co-pilot: A Generative AI interface for policymakers to brainstorm and instantly simulate the impact of mitigation strategies (e.g., "What if we implement an EV-only zone?") in a dynamic "Policy Sandbox".
🏗️ System Architecture
Our platform is built on a scalable, cloud-native architecture. Data flows from various sources into our Data Fusion Engine on Google Cloud, where it is processed and stored in BigQuery. This unified data then feeds our core AI modules, with the final predictions and insights served via an API to our user-facing dashboards.
*(You can embed the architecture diagram image here)
code
Code
![Aura System Architecture]([link_to_your_architecture_diagram_image_in_the_repo.png])
💻 Technology Stack
Backend: Python, FastAPI
Data Science & ML: Pandas, GeoPandas, Scikit-learn, XGBoost, PyTorch (for GNN)
Cloud Platform: Google Cloud Platform (GCP)
Storage: Google Cloud Storage & BigQuery
Compute & AI: Vertex AI, Cloud Functions
Geospatial: Google Earth Engine API, QGIS/ArcGIS for analysis
Frontend: React, Deck.gl / Mapbox GL JS
Generative AI: Google Gemini Pro API
📊 Project Status
Current Phase: Milestone 1 - Predictive Model MVP (Complete)
We have successfully developed and validated the core predictive model ("Sentinel Engine" MVP).
✅ Acquired and cleaned real-world data for Gurugram.
✅ Fused CPCB ground station data with MODIS AOD satellite data.
✅ Trained a baseline XGBoost model with a validated R² score of [Your R² Score, e.g., 0.82] on unseen test data.
The project is now progressing to Phase 2: implementing the advanced Deep Learning model and developing the backend API.
🚀 Getting Started
Instructions on setting up the project locally.
Prerequisites
Python 3.9+
Google Cloud SDK configured
Access to a Google Earth Engine account
[...]
Installation
Clone the repository:
code
Sh
git clone https://github.com/[your-username]/aura-project.git
cd aura-project
Create a virtual environment and install dependencies:
code
Sh
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
Set up your environment variables (.env file):
code
Sh
# copy .env.example to .env and fill in your GCP credentials
cp .env.example .env
USAGE
To run the data processing pipeline:
code
Sh
python scripts/process_data.py
To train the baseline model:
code
Sh
python models/train_baseline.py
🗺️ Roadmap
[✔] Milestone 1: Predictive Model MVP
[○] Milestone 2: GNN Implementation & API Development
Implement the Graph Neural Network model.
Develop a FastAPI backend to serve model predictions.
Build the first interactive dashboard prototype.
[ ] Milestone 3: Full Prototype & "Detective Engine"
Develop the source attribution module.
Integrate all modules into a cohesive dashboard.
[ ] Milestone 4: "Strategist Co-pilot" & Final Polish
Integrate the Generative AI policy sandbox.
User testing and final refinements.