# 🌌 ExoNovaPioneers – A World Away (NASA Space Apps Challenge 2025)

## 🔭 Project Overview

**ExoNovaPioneers** is an AI + AR/VR-powered platform designed to help scientists, students, and the public explore exoplanets.
It leverages NASA’s exoplanet archives and ML/AI models to evaluate habitability while offering immersive 3D visualizations of planetary systems.

Challenge: **A World Away: Hunting for Exoplanets with AI**

---

## ⚙️ Implementation Details

### 1. **Data Pipeline**

* **Sources**: NASA Exoplanet Archive (confirmed exoplanet datasets, stellar parameters, orbital data).
* **Cleaning & Preprocessing**:

  * Handling missing values, normalizing features (stellar radius, effective temperature, orbital distance).
  * Label engineering for “potential habitability” using Earth Similarity Index (ESI).
* **Storage**: Cleaned dataset stored in **PostgreSQL** and accessed via APIs.

---

### 2. **AI/ML Models**

* **Habitability Prediction**:

  * Trained using **Random Forests** + **Gradient Boosting (XGBoost/LightGBM)**.
  * Features: surface temperature, stellar flux, eccentricity, planetary mass & radius.
  * Output: Habitability Probability Score (0–1).
* **Natural Language Layer**:

  * Integrated with **LLMs** (GPT-based) for Q&A on exoplanets.
  * Example: *“Show me planets similar to Earth with surface temps between 250–300K.”*

---

### 3. **Backend Services**

* Built with **Spring Boot (Java)** + **Python FastAPI microservices** for ML models.
* Exposes REST APIs:

  * `/predictHabitability` → returns score + habitability class.
  * `/planetarySystem/{id}` → fetches orbital/stellar data for visualization.

---

### 4. **Frontend Platform**

* **Web App** using **React + Three.js** for 3D visualization.
* **Features**:

  * Interactive planetary orbits.
  * Habitability heatmaps (color-coded by probability score).
  * Side panel with AI-driven insights (LLM responses).

---

### 5. **Immersive Visualization (AR/VR)**

* Built with **Unity3D + WebXR** for browser and headset support.
* User can:

  * “Fly” through exoplanetary systems.
  * View atmospheres, orbital paths, habitable zones in immersive 3D.
* Future scope: Support **Oculus/Meta Quest** for deeper exploration.

---

### 6. **Deployment**

* **Containerized with Docker**, deployed on **AWS/GCP**.
* ML models hosted via **NVIDIA GPU instances** for real-time inference.
* Frontend hosted on **Vercel/Netlify** for easy access.

---

## 🚀 Tech Stack

* **AI/ML**: Python, Scikit-learn, TensorFlow, XGBoost
* **Backend**: Spring Boot, FastAPI, PostgreSQL
* **Frontend**: React, Three.js, Tailwind
* **Visualization**: Unity, WebXR
* **Infra**: Docker, AWS/GCP

---

## 🌍 Impact

* **NASA Scientists**: Faster analysis of habitability likelihood.
* **Students & Educators**: Immersive, interactive learning of exoplanets.
* **Public Outreach**: Space exploration brought closer to everyone.

---
