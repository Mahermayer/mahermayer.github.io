---
title: "ML-Based Temperature Control with Anomaly Detection (Smart Buildings)"
date: 2025-01-25
summary: Integration of anomaly detection, LSTM forecasting, and PID control to defend against false data injection (FDI) in IoT-enabled HVAC systems.
tags: [CPS-ML, Anomaly Detection, Smart Buildings, LSTM, PID, FDI Attack]
---

In IoT-enabled smart buildings, temperature sensors are vulnerable to **false data injection (FDI) attacks** that can mislead controllers and compromise safety.  
We propose a **multi-layer ML + control pipeline** that enhances resilience:

### Pipeline
- **Random Forest Classifier** detects **FDI anomalies** in IoT sensor data.  
- **LSTM forecasting** predicts safe temperature setpoints, isolating suspicious signals.  
- **PID controller** enforces corrective action in real time to maintain HVAC stability.  

![FDI Anomaly-Aware HVAC Control](/uploads/smart_home_ML.png)

### Highlights
- Prevents **energy misuse** and **unsafe thermal conditions**.  
- Provides adaptive protection against **sensor/network attacks**.  
- Demonstrates **cyber-physical resilience** by fusing anomaly detection with control.  

**Takeaway.** Anomaly-aware control strengthens both **security and efficiency**, making smart buildings safer under adversarial conditions.
