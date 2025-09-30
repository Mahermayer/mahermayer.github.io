---
title: "Context-Aware Autonomy under Perception Gaps"
date: 2025-01-05
summary: LaneNet-style UNet with Squeeze-and-Excitation + depthwise separable convolutions and loss tailoring to survive missing/occluded lanes and adversarial noise.
tags: [Autonomous Vehicles, Lane Keeping, UNet, LaneNet, SE, DepthwiseConv, Robustness]
featured_image: "/uploads/ICRA_UNet.jpg"
---

We mimic **adversarial settings** (missing/occluded lane markings, noise, motion blur) and train a **LaneNet-style UNet** with two robustness tweaks:

1) **Depthwise-Separable Convs (DWConv + Pointwise)** → lower params, better inductive bias  
2) **Squeeze-and-Excitation (SE)** → channel-wise attention to stabilize features

### Architecture (LaneNet-UNet)
![UNet overview](/uploads/ICRA_UNet.jpg)

**Depthwise + 1×1 pointwise**
![Depthwise](/uploads/DWConv_Depthwise.jpg)
![Pointwise](/uploads/DWConv_Pointwise.jpg)

**Squeeze & Excitation**
![SE](/uploads/Squeeze_Excite.jpg)

### Losses
- **Dice + BCE** for lane mask
- **Centerline offset loss** to keep predicted midline plausible when one lane edge disappears
- **Temporal smoothness** (β-TV) to suppress jitter frame-to-frame

### Demo (context-aware lane keeping)
<video src="/uploads/ICRA_Final.mp4" controls playsinline style="width:100%;"></video>

**Outcome.** When one lane edge vanishes, the model extrapolates centerline from context and history, keeping control smooth. No more panic-swerves when paint quality… isn’t.
