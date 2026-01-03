## ML API – Crowd & Panic Intelligence Service
A **production-ready Machine Learning API** that serves real-time predictions for **crowd load, panic indicators, and risk signals**.  
Designed to seamlessly integrate with websites, dashboards, and surveillance systems.

---

## Purpose
This API acts as the **intelligence layer** for crowd & panic detection systems.  
It exposes ML models via REST endpoints to:
- Predict crowd footfall
- Consume real-time inputs (camera data, weather, calendar, events)
- Continuously store actual counts for retraining
- Serve predictions with low latency

---

## Core Capabilities
- Ensemble ML inference (CatBoost + LightGBM / XGBoost + LSTM)
- Feature-engineered predictions (calendar, weather, festivals)
- RESTful API using FastAPI
- MongoDB for real-time data storage
- CORS-enabled for frontend integration
- Scalable & modular architecture
---
## Architecture Overview
Client / Website / Dashboard
|
v
ML API (FastAPI)
|
├── Feature Engineering Layer
├── ML Ensemble Models
├── Panic / Risk Logic
|
MongoDB (Actuals + Logs)

---

## Tech Stack
- **Python**
- **FastAPI**
- **Uvicorn**
- **Scikit-learn**
- **CatBoost**
- **LightGBM / XGBoost**
- **TensorFlow (LSTM)**
- **MongoDB**
- **Joblib**

---

## Project Structure
ml_api/
├── app.py
├── test_clean_encoded_2.csv
├── models/
│ ├── Blended_model.pkl
│ └── scalers.pkl
├── requirements.txt
└── README.md
---
## Installation
```bash
git clone https://github.com/your-username/ml_api.git
cd ml_api
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
**Run the API**
```bash
uvicorn app:app --host 0.0.0.0 --port 8000
```
**ML Details (High Level)**
-LSTM → captures temporal crowd patterns
-Tree Models → capture nonlinear interactions
-Meta Model → combines all predictions
-Feature Engineering includes:
  -Day / month cyclic encoding
  -Festival impact
  -Weather influence
  -Lag & rolling statistics

**Data Storage**
MongoDB
Stores daily actual footfall
Stores predictions vs reality
Enables continuous retraining


👤 Author
Jinay Jain
B.Tech, IIT (ISM) Dhanbad
Smart India Hackathon Winner

