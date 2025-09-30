---
title: "Hands-on Network & IoT Security Experiments"
date: 2025-02-08
summary: Practical implementation of client-server communication, IoT protocols, and classical network attacks to study CPS and IoT vulnerabilities.
tags: [Cybersecurity, IoT Security, Network Security, Protocol Attacks, CPS]
featured_image: "/uploads/network_iot.jpg"
---

This work explores **low-level networking and IoT security**, focusing on both system setup and adversarial attack implementations.  
Unlike CTF challenges, these are **protocol-grounded experiments** conducted in lab and IoT testbeds.

## System Setup (IoT / Smart-HVAC)
Part of this work used a Smart-HVAC testbed (sensor array → ThingSpeak telemetry → MATLAB control + Node.js MQTT broker on Raspberry Pi).  
The full slide deck describing the IoT architecture, sensors, and control cases is available in the project materials.  

**Key components**
- TCP/UDP client-server apps in C; DNS config and NetFilter firewall rules.  
- Raspberry Pi MQTT broker/client (Node.js) for telemetry and control.  
- Telemetry visualized via ThingSpeak; control logic prototyped in MATLAB (HVAC control cases).  

![ThingSpeak/MQTT integration](/uploads/thingspeak.png)  
![HVAC Control Cases](/uploads/HVAC_Table.png)  

I also worked on different attack implementation using 3 different Virtual Machines (Windows, Kali, Ubuntu).
## Attack Implementations (lab)
- **Packet sniffing & spoofing** with Scapy.  
- **TCP Reset & port scanning** with Nmap.  
- **Man-in-the-Middle (MiTM), ARP/DNS spoofing** attacks and DNS cache poisoning.  
- **DoS/Traffic flood attacks** to measure service degradation.  
- **Mitnick-style TCP session manipulations** to study session hijacking.  

## Highlights
- Implemented and hardened IoT stacks (MQTT + NetFilter) in Raspberry Pi testbeds.  
- Demonstrated the end-to-end impact of protocol attacks on telemetry, control, and resultant HVAC behavior.  
- Bridged practical protocol engineering with adversarial testing — build it, break it, then fix it.  

**Takeaway.** These experiments deepen understanding of real-world protocol security and control safety in IoT/CPS systems, and they directly informed mitigation steps presented in the Smart-HVAC slides.
