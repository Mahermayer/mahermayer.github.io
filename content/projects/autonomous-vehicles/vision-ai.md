---
title: Vision AI-based Autonomous Driving
date: 2025-01-01
summary: Deep learning-driven lane following and perception systems with adversarial robustness in degraded environments.
tags:
  - Autonomous Vehicles
  - Computer Vision
  - ROS
  - YOLO
  - UNet
  - ViT
  - Duckietown
links:
  - type: github
    url: https://github.com/your-repo   # <-- replace with actual repo if you want
  - type: external
    url: https://www.duckietown.org/    # optional reference
featured: true   # <-- will highlight this project in grids
---

This project implements **vision-based lane following and control** pipelines for autonomous driving.  
I integrated **YOLO, UNet, and Vision Transformers (ViT)** for real-time perception tasks such as lane detection, object recognition, and traffic sign handling.  

On the control side, I deployed **PID and MPC controllers** in ROS to ensure smooth navigation.  
The system was evaluated both in the **Duckietown testbed** and in simulation environments like CARLA.  

Additionally, I designed **adversarial robustness testing** (FGSM, PGD, DeepFool) to evaluate how perception modules degrade under adversarial conditions, and proposed defense strategies for resilient autonomy.
