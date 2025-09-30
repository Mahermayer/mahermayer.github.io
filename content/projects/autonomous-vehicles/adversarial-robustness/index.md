---
Title: Adversarial Robustness of AI Models in Autonomous Vehicles
Date: 2025-01-10
Summary: Analyzing adversarial threats and mitigation strategies for AI models in autonomous vehicles.
tags: [Adversarial AI, Robustness, FGSM, PGD, DeepFool, UAP, ZOO, YOLO, UNet, ViT]
---

This project investigates **adversarial robustness** in AV perception. Adversarial AI can be broadly categorized into:

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
- Object Detection Models (traffic signs/lights/pedestrian)  
- Segmentation Networks (lane segmentation)  
- ViT (auxiliary classification)  
---
