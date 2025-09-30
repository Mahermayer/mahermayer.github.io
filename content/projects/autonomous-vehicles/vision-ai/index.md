---
title: "Vision AI–based Autonomous Driving (Reactive Rule Following)"
date: 2025-01-01
summary: YOLO + PID pipeline for traffic-rule following in Duckietown, running with Dockerized ROS server integration.
tags: [Autonomous Vehicles, Computer Vision, ROS, PID, YOLO, Docker]
featured: true
featured_image: "/uploads/Reactive_velocity.jpg"
---

## Setup  
The system was deployed on **Duckietown** using **Dockerized ROS containers**.  
- A **ROS server** ran YOLO-based perception modules (traffic lights, stop signs, lane cues).  
- Control commands (`Twist2DStamped`) were streamed over to the Duckiebot wheel command ros topic.  
- Duckietown’s modular **Docker stack** (dt-core, dt-car-interface, dt-duckiebot-interface) provided a clean integration with the robot’s drivers and control nodes.  

![ROS server architecture](/uploads/ros_server.png)  
![Duckietown code hierarchy](/uploads/code_hierarchy.png)  

## Control  
- Perception: **YOLO + lane heuristic**  
- Decision: Finite-state rule engine (stop, go, lights)  
- Execution: **PID controller** for velocity + heading, publishing to `car_cmd_switch_node/cmd`  

## Results  
- Robust **lane following + traffic-rule compliance** (stop + lights) on both rectangular and curved maps.  
- Smooth **normalized velocity profiles** with consistent braking and recovery.  

![Normalized velocity on two maps](/uploads/Reactive_velocity.jpg)  

## Demo  
<video src="/uploads/Yolo1.mp4" controls playsinline style="width:100%;"></video>  
<video src="/uploads/Yolo2.mp4" controls playsinline style="width:100%; margin-top:0.5rem;"></video>  

**Takeaway.** A Dockerized YOLO + PID pipeline with ROS messaging achieves stable small-scale autonomy and provides a modular base for scaling toward context-aware and adversarially robust AVs.  
