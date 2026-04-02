# 💧 AquaGuard AI: Water-Borne Disease Prediction System

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20App-brightgreen?style=for-the-badge&logo=render)](https://water-quality-frontend-58dl.onrender.com)
[![GitHub Stars](https://img.shields.io/github/stars/Aashutosh-357/waterborne-disease-prediction?style=for-the-badge)](https://github.com/Aashutosh-357/waterborne-disease-prediction)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

## 🛡️ AI-Powered Early Warning Surveillance

**AquaGuard AI** is a sophisticated full-stack surveillance system designed to forecast water-borne disease outbreaks (specifically **Cholera** and **Typhoid**) with up to **88% accuracy**. By analyzing environmental, meteorological, and water quality parameters, the system provides health authorities with a **1–3 week lead time** to implement life-saving preventive measures.

---

## 📽️ Key Features

- **🧠 Predictive Intelligence:** Real-time risk scoring using high-performance **XGBoost Ensemble Models** trained on 5.25M+ records.
- **📊 Analytics Dashboard:** Interactive visualizations for deep dives into environmental trends and model performance metrics.
- **📲 Mobile First:** Fully responsive UI built with **Tailwind CSS v4** and **Shadcn UI**, optimized for field health workers.
- **⚡ High Performance:** Optimized for fast inference and real-time feedback with **React 18** and **FastAPI**.

---

## 🏗️ Technical Architecture

### **Core Stack**

| Layer | Technologies |
| :--- | :--- |
| **Frontend** | ![React](https://img.shields.io/badge/react-%2320232a.svg?style=flat&logo=react&logoColor=%2361DAFB) ![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=flat&logo=vite&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=flat&logo=tailwind-css&logoColor=white) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=flat&logo=typescript&logoColor=white) |
| **Backend** | ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi) ![Python](https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54) ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white) |
| **Data & ML** | ![XGBoost](https://img.shields.io/badge/XGBoost-EB2529?style=flat&logo=xgboost&logoColor=white) ![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikit-learn&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white) |
| **DevOps** | ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white) ![Render](https://img.shields.io/badge/Render-%46E3B7?style=flat&logo=render&logoColor=white) |

### **Information Synthesis**
The model processes a comprehensive multi-modal dataset:
-   **🌍 Environmental:** Rainfall (mm), Temperature (°C), Humidity (%), Flooding status.
-   **💧 Water Quality:** pH Levels, Chlorine treatment status, Source type (Piped, Well, River).
-   **👥 Demographics:** Population Density, Area Classification (Urban/Rural).

---

## 🚀 Getting Started

### **1. Rapid Deployment (Docker)**
The most reliable way to run AquaGuard AI is using Docker.

```bash
# Clone the repository
git clone https://github.com/AmanKushwaha47/Water_Quality_Prediction.git
cd Water_Quality_Prediction

# Start the entire ecosystem
docker compose up --build
```

Access the system:
-   🌐 **Frontend:** `http://localhost:5173`
-   📡 **API Docs (Swagger):** `http://localhost:8000/docs`

### **2. Manual Local Setup**

#### **Backend**
```bash
cd Backend
python -m venv venv
source venv/bin/activate # or venv\Scripts\activate on Windows
pip install -r requirements.txt
uvicorn app.main:app --reload
```

#### **Frontend**
```bash
cd Frontend
npm install
npm run dev
```

---

## 📡 API Reference

### **Epidemiological Risk Prediction**
`POST /api/predict`

**Payload:**
```json
{
  "area_type": "Urban",
  "population_density": 1200,
  "water_source": "Piped",
  "water_treatment": "Chlorinated",
  "ph_level": 7.2,
  "avg_temp": 28.5,
  "avg_rainfall": 150.0,
  "avg_humidity": 75.0,
  "flooding_status": "No"
}
```

**Response:**
```json
{
  "prediction": 1,
  "probability": 0.92,
  "risk_level": "High Risk",
  "recommendation": "Immediate intervention: Chlorine distribution and public warnings."
}
```

---

## 📁 Project Structure

```text
.
├── Backend/          # FastAPI App & Machine Learning Models
│   ├── app/          # API Core & Business Logic
│   ├── src/          # ML Pipeline & Utils
│   └── data/         # Datasets & Pickled Models
├── Frontend/         # React 18 / Vite / Tailwind UI
│   ├── src/          # Components, Pages & Styles
│   └── public/       # Static assets
├── docker-compose.yml # Container orchestration
└── render.yaml       # Infrastructure-as-code for deployment
```

---

## 📄 License & Attribution
-   **Capstone Project:** Developed as an AI-driven Public Health surveillance solution.
-   **Design:** UI inspired by modern glassmorphism principles and Shadcn/UI.
-   **Dataset:** Sourced from Regional Health Department records on water-borne disease incidence.

---

<div align="center">
  Developed with ❤️ for Global Public Health.
</div>
