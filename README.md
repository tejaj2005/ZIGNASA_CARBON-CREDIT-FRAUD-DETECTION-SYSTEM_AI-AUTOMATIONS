# ZIGNASA_CARBON-CREDIT-FRAUD-DETECTION-SYSTEM_AI-AUTOMATIONS

# Carbon Credit Fraud Detection System – n8n Workflow Documentation

## 🚀 Overview
The **Carbon Credit Fraud Detection System** is an AI-powered, multi-source validation workflow built using **n8n**, designed to detect fraudulent carbon credit claims.  
The system cross-verifies emissions using:

- Satellite environmental data  
- Real-time air quality & pollutant history  
- Local energy usage patterns  
- Anomaly detection logic  
- AI-powered fraud scoring (Qwen 2.5 14B Instruct)

It automatically generates fraud reports, dashboards, and email alerts for authorities.

---

## 📌 Problem Statement
Carbon credits can be manipulated by industries that:

- Over-report emission reductions  
- Hide actual CO₂ output  
- Fake documentation  
- Claim unrealistic sustainability improvements  

There is **no automated system** that validates carbon credit claims using **real-world environmental data**.

---

## 💡 Solution Summary
This project builds a **multi-source fraud detection engine** that:

### ✔ Fetches real environmental and activity data  
From:
- Open-Meteo Air Quality API  
- Open-Meteo Weather Forecast / Energy Signals API  
- Satellite Position API (demo satellite)  

### ✔ Merges all datasets into one structured object  
### ✔ Runs anomaly detection logic  
- High emission spikes  
- Energy vs emission mismatch  
- Sudden pollutant jumps  
- Location inconsistency  
- Usage pattern irregularities  

### ✔ Sends merged dataset to LLM (Qwen2.5-14B)  
AI generates:
- Fraud probability (0–100%)  
- Anomalies detected  
- Final judgement  
- Recommended actions  

### ✔ Generates automatic reports  
- **Dashboard HTML**  
- **FraudReport.pdf**  
- **Export.csv**  

### ✔ Sends updates via Email / Telegram

---

## 🌐 APIs Used

### **1️⃣ Emission History API (Air Quality)**
