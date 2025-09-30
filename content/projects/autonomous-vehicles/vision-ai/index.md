---
title: "Vision AI–based Autonomous Driving (Reactive Rule Following)"
date: 2025-01-01
summary: YOLO + PID pipeline for traffic-rule following with speed profiling on Duckietown; normalized velocity profiles on rectangular vs curved maps.
tags: [Autonomous Vehicles, Computer Vision, ROS, PID, YOLO]
featured: true
featured_image: "/uploads/Reactive_velocity.jpg"   # local to this folder
---

**Pipeline.** Camera → **YOLO** (objects/lights/signs) + lane segmentation heuristic → finite-state rule engine → **PID** longitudinal/heading controllers → `/wheels_driver_node/wheels_cmd`.

**Highlights**
- Real-time reactive rule following (stop sign + traffic lights).
- Stable control on Map A (rectangular) and Map B (curved); see normalized velocity profiles.
- ROS message interface: `WheelsCmdStamped` (not `/cmd_vel`) for Duckietown.

## Demo (YOLO + PID)
<video src="/uploads/Yolo1.mp4" controls playsinline style="width:100%;"></video>

<video src="/uploads/Yolo2.mp4" controls playsinline style="width:100%; margin-top:0.5rem;"></video>

## Results
![Normalized velocity on two maps](Reactive_velocity.jpg)

**Takeaways.** PID with tight anti-windup and a rule-based scheduler is plenty for small-scale AVs—until perception gets weird. Then we need context and robustness (next two projects).
