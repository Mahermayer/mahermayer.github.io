---
title: "Context-Aware Autonomous Driving under Degraded Environments"
date: 2025-01-05
summary: LaneNet (U-Net with depthwise separable convolutions and SE attention) for autonomous driving under degraded and adversarial lane environments.
tags: [Autonomous Vehicles, Lane Keeping, UNet, LaneNet, DWConv, SE Blocks, Context-Aware]
---

This work explores **context-aware autonomous driving** when lane markings are degraded, occluded, or adversarially perturbed.  

We proposed **LaneNet**, a U-Net modified with **depthwise separable convolutions** and **squeeze-and-excitation attention**, designed to provide lightweight yet robust lane segmentation.  
![LaneNet overview](/uploads/ICRA_UNet.jpg)

We utilize a **spatio-temporal context** to infer lane centers when lane pixels are missing or corrupted. This enables smooth control in degraded and adversarial conditions.  

---

## System Setup
- Same base setup as in **Vision AI-based Autonomous Driving**, running on Duckietown with Dockerized ROS nodes.  
- Includes robustness evaluation under **physical degradation** (faded/missing lanes) and **adversarial AI attacks**.  
![System pipeline under degraded/adversarial environment](/uploads/ICRA_Archi.jpg)

---

## Demo
<video src="/uploads/Trajectory.mp4" controls playsinline style="width:100%;"></video>

---

**Takeaway.** With context-aware reasoning, the system remains stable even when lane markings are incomplete or perturbed by adversarial inputs.
