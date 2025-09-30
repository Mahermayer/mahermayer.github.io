---
title: "Adversarial Robustness of Vision Models for AV"
date: 2025-01-10
summary: Adversarial attacks in Vision AI.
tags: [Adversarial AI, Robustness, FGSM, PGD, DeepFool, UAP, ZOO, YOLO, UNet, ViT]
---

This project investigates **adversarial robustness** in AV perception.  
Adversarial AI can be broadly categorized into:

- **White-box attacks** → attacker knows the model and gradients  
- **Black-box attacks** → attacker uses surrogate models and queries  

![Black-box vs White-box](/uploads/BW.png)

---

## Framework
We explore **systematic attacks** against vision models used in AV:

- **FGSM / PGD** → gradient-based ℓ∞ & ℓ2  
- **DeepFool** → minimal ℓ2  
- **ZOO** → gradient-free, query-efficient  
- **UAP** → universal, image-agnostic perturbations  

![Adversarial Framework](/uploads/Black_n_White.png)

**Targets:**  
- YOLO (traffic signs/lights)  
- UNet (lane segmentation)  
- ViT (auxiliary classification)  

---

## Status
This is an **ongoing work** — experiments are being conducted to quantify attack severity and cross-model transferability. Results will be reported after evaluation.

---
