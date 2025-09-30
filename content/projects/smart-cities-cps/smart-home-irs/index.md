---
title: "Model-Based Intrusion Response System for Smart Homes"
date: 2025-02-20
summary: MDP-based self-protection framework for smart homes, enabling autonomous, real-time defense against cyber-physical attacks on IoT and CPS devices.
tags: [CPS-ML, MDP, Cybersecurity, Reinforcement Learning, Simulink]
featured_image: "/uploads/CCI_Smart_home.png"
show_date: false
show_read_time: false
show_read_more: false
---

Smart homes are a critical layer of **cyber-physical systems (CPS)** in modern cities, but they are increasingly targeted by adaptive cyber-attacks on IoT sensors and controllers. Traditional static defenses and pure IDS approaches struggle with low-latency, system-aware response.  

To address this, we developed a **Model-Based Intrusion Response System (IRS)** built around a Markov Decision Process (MDP). The project starts by modeling the physical CPS (HVAC/temperature control) in Simulink, then models attacker behaviors, and finally derives offline policies that enable fast, effective runtime responses.

![Smart home IRS attack model](/uploads/CCI_Smart_home.png)

## Approach
1. **System Modeling**  
   - Built a realistic smart-home temperature control model in **MATLAB/Simulink** using bang-bang controller to capture sensing, actuation, and control loops. This provides the physical environment and timing semantics used for all evaluations.  
   ![Temperature Control Simulink Model](/uploads/Room.png)

2. **Threat modeling (attack profiles)**  
   - Emulated a comprehensive attacker model covering: **replay, sniffing, eavesdropping, false data injection, spoofing, MiTM, code injection, malware injection, jamming, and DDoS**.  

3. **Defensive capabilities & system configurations**  
   - Modeled actionable defenses available on the smart-home platform: **activate firewall, data encryption, deploy honeypot, quarantine host, firmware update, system reboot, manual resolution**, etc. Each defensive action has an associated cost and latency captured in the environment model.

4. **MDP formulation & policy derivation**  
   - Designed a reward function that balances **security benefit** (reduction in system compromise / control error) against **operational cost** (latency, user disruption, resource usage).  
   - Solved the MDP offline using Monte-Carlo lookahead to produce low-latency policies suitable for real-time execution.

5. **Evaluation & validation**  
   - Deployed offline policies in the Simulink testbed and measured control stability, cumulative security reward, and response latency.  
   - Benchmarked the MDP policy against baseline random/heuristic responses and a DQN baseline. Results show superior stability and lower latency for the offline MDP policy.

![IRS state-action dynamics](/uploads/MDPAction.png)

## Results
- The MDP-based IRS consistently outperformed baseline strategies in cumulative reward and system stability.  
- Offline policy execution reduced average response latency to **~0.48 ms** (vs ~2.5 ms for online learning in our setup).  
**Takeaway.** Protecting smart-home CPS requires system-aware defenses. By combining Simulink-based CPS modeling with MDP planning and offline policy synthesis, the IRS enables fast, cost-aware responses that preserve both safety and service continuity.
