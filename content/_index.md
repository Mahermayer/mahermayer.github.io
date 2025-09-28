---
title: ''
date: 2022-10-24
type: landing

design:
  spacing: '2rem'

sections:
  - block: resume-biography
    content:
      username: admin
      text: ''
      button:
        text: Download CV
        url: uploads/resume.pdf
    design:
      css_class: hbx-bg-gradient
      avatar:
        size: medium
        shape: circle
    
  - block: markdown
    content:
      title: Research Interests
      text: |-
        <div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 0.5rem 2rem;">
          <ul>
            <li>Autonomous Vehicles</li>
            <li>Adversarial AI</li>
            <li>Cybersecurity</li>
          </ul>
          <ul>
            <li>Cyber-Physical Systems</li>
            <li>AI Safety & Ethics</li>
          </ul>
        </div>
    
  - block: resume-experience
    content:
      title: Education & Experience
      username: admin
    design:
      view: card
      columns: 2
      date_format: 'January 2006'
      is_education_first: true



  - block: resume-skills
    content:
      title: Skills
      username: admin
    design:
      view: card
      columns: 2
      css_class: no-top-margin
  - block: markdown
    content:
      title: Awards
      text: |-
        ### Diamond Badge (97th Percentile) – NCL Spring 2025  
        ![NCL Badge](uploads/NCL.jpg)  
        Ranked top 3% nationally among ~8,500 participants.  

        ### 3rd Place – WVU AI Symposium Poster Contest  
        ![WVU AI Symposium](uploads/WVU_AI_Symp.jpg)  
        Poster: *AI in Autonomous Vehicles Under Siege*.  

        ### Best Poster Award – IEEE SmartComp 2024  
        ![SmartComp 2024](uploads/SmartComp_2024.jpg)  
        Poster: *OpenCyberCity Testbed's Recent Progress in Smart City Management*.  

---
