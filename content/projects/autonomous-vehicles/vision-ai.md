---
title: "Vision AI-based Autonomous Driving"
date: 2025-01-01
summary: Deep learning-driven lane following and perception systems with adversarial robustness.
tags:
  - Autonomous Vehicles
  - Computer Vision
  - ROS
  - YOLO
  - UNet
  - ViT
featured: true
# type: projects  
---

This project implements **vision-based lane following and control** pipelines for autonomous driving.  

I integrated **YOLO, UNet, and Vision Transformers (ViT)** for real-time perception tasks such as lane detection, object recognition, and traffic sign handling.  

On the control side, I deployed **PID and MPC controllers** in ROS to ensure smooth navigation.  
The system was evaluated in **Duckietown** and **CARLA**.  

I also designed **adversarial robustness tests** (FGSM, PGD, DeepFool) to evaluate how perception modules degrade under adversarial conditions.
