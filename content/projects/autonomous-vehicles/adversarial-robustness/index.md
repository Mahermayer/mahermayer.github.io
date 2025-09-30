---
title: "Adversarial Robustness of Vision Models for AV"
date: 2025-01-10
summary: Systematic attacks (FGSM, PGD, DeepFool, ZOO, UAP) on YOLO/UNet/Vision-Transformer perception with stress tests relevant to driving.
tags: [Adversarial AI, Robustness, FGSM, PGD, DeepFool, UAP, ZOO, YOLO, UNet, ViT]
featured_image: "/uploads/Black_n_White.png"
---
We evaluate **white-box** and **black-box** attacks on AV perception:

- **FGSM / PGD:** gradient-based ℓ∞ & ℓ2  
- **DeepFool:** minimal ℓ2  
- **ZOO:** gradient-free (query-efficient)  
- **UAP:** image-agnostic perturbations

**Targets:** YOLO (traffic signs/lights), UNet (lanes), ViT (auxiliary classification).

**Metrics:** mAP (YOLO), Dice/IoU (UNet), control-level impact (velocity/omega deviations).

![Threat landscape](/uploads/Black_n_White.png)
![Black-box vs White-box](/uploads/BW.png)

### Findings (abridged)
- **PGD** most damaging to UNet; a small ε causes large centerline drift → steering oscillations.
- **UAP** transfers across backbones; YOLO degrades on stop/traffic-light classes → TTL violations.
- **Simple defenses** (RandAug, input JPEG recompress, test-time augment) help a little; **SE + temporal smoothing** helps more. Ultimately you’ll want **adversarial training** or certified bounds for safety-critical deployments.

> Bottom line: if your perception stack isn’t tested against these, you’re flying VFR into a thunderstorm.
