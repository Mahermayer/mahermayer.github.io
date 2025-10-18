---
title: "Adversarial Robustness in Cloud-Assisted Autonomous Driving"
date: 2025-10-18
summary: Hardware-in-the-loop IoV testbed evaluating YOLOv8 perception and network resilience under coordinated adversarial attacks.
weight: 1   # 👈 move this up if you want it to show first
tags: [Autonomous Vehicles, Internet of Vehicles, YOLOv8, Adversarial AI, Network Security, Duckietown]
featured: true
---

## Overview  
This work introduces a **hardware-in-the-loop Internet of Vehicles (IoV) testbed** for studying the joint impact of **adversarial AI** and **network-layer attacks** on cloud-assisted autonomous driving.  
- **Perception Layer:** A YOLOv8-based detector faces white-box adversaries (FGSM, FGSM-GT, PGD).  
- **Communication Layer:** Network perturbations (delay, packet loss) are injected using the **MITRE ATT&CK** threat framework.  
- **Integration:** The testbed couples a **Duckiebot edge client** with a **cloud perception–control server**, achieving real-time closed-loop testing of cross-layer vulnerabilities.

![IoV Testbed Architecture](/uploads/iov_testbed.jpg)  

## Experimental Design  
- **Hardware Setup:** Duckiebot with Jetson edge device connected via TCP to a cloud server (RTX A2000).  
- **Perception:** YOLOv8n trained on 2,414 annotated Duckietown frames for stop signs, traffic lights, and vehicles.  
- **Attacks:**  
  - FGSM, FGSM-GT, and PGD perturbations at ϵ = {0.01, 0.02, 0.04}  
  - Network delay (100–250 ms) and packet loss (0.5–5%) injected via `tc netem`.  
- **Control:** PID-based lane following and traffic-rule compliance evaluated under perturbed feedback loops.  

![Detection under adversarial perturbations](/uploads/adv_yolo.png)  

## Results  
- **Perception degradation:** PGD reduces YOLOv8 **precision and recall to 0.22 and 0.15** at ϵ = 0.04.  
- **Network degradation:** Delay ≥ 150 ms or loss ≥ 2% causes **trajectory drift and stop-sign violations**.  
- **Cross-layer effect:** Even modest attacks in either domain cause cascading control failures, highlighting the need for **joint resilience across AI and communication layers**.  

![Vehicle trajectories under network delay/loss](/uploads/network_impact.png)  

## Demo  
<video src="/uploads/icc_2026.mp4" controls playsinline style="width:100%;"></video>  

## Takeaway  
The study demonstrates that **minor perturbations at either the perception or communication layer can destabilize cloud-assisted AVs**.  
Future work will focus on **cross-layer defense mechanisms**, including latency-tolerant control, adversarially trained perception, and secure communication middleware for the Internet of Vehicles.
