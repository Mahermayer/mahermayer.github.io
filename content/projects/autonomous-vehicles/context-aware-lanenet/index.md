---
title: "Context-Aware Autonomy under Perception Gaps"
date: 2025-01-05
summary: LaneNet (U-Net with depthwise separable convolutions and SE attention) for autonomous driving under degraded lane environments.
tags: [Autonomous Vehicles, Lane Keeping, UNet, LaneNet, DWConv, SE Blocks, Context-Aware]
featured_image: "/uploads/ICRA_UNet.jpg"
---

This work explores **context-aware lane keeping** when lane markings are degraded or partially missing.  
We adapt a **LaneNet-inspired U-Net**, modified with **depthwise separable convolutions** and **squeeze-and-excitation attention**, to provide lightweight yet robust lane segmentation.

Instead of relying solely on per-frame predictions, the system leverages **spatio-temporal context** to infer lane centers under missing pixels and visual noise. This stabilizes control on Duckietown maps where conventional lane-following pipelines fail.

---

## Setup
- **Same as Vision AI-based Autonomous Driving.

---

## Demo
<video src="/uploads/ICRA_Final.mp4" controls playsinline style="width:100%;"></video>

---

**Takeaway.** With context-aware reasoning, the system remains stable even when under degraded lane environemnts.
