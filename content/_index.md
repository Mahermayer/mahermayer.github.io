---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/resume.pdf
      headings:
        about: 'Welcome!🚗🤖🔒'
        education: ''
        interests: 'Research Interests'
        work: 'Experience'
    design:
      # Apply a gradient background
      css_class: hbx-bg-gradient
      # Avatar customization
      avatar:
        size: medium
        shape: circle

  - block: resume-skills
    content:
      title: Skills    
      username: admin
    design:
      view: list
      columns: 3
      css_class: no-top-margin
    
  - block: collection
    content:
      title: Selected Publications
      text: >
        A few of my recent and representative research works.  
        [View full list →](/publications/)
      filters:
        folders:
          - publications
      count: 3   # show 3 here; set to 50 or remove to show all
    design:
      view: citation
      fill_image: false
      columns: 1
      show_date: false
      show_read_time: false
      show_read_more: false
    
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
