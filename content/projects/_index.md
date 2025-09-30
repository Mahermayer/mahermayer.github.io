---
title: 'Projects'
date: 2024-05-19
type: landing

design:
  spacing: '5rem'

sections:
  - block: collection
    content:
      title: Projects
      text: >
        Organized into four categories: Autonomous Vehicles, Cybersecurity, Smart Cities & CPS, and Anomaly Detection.  
        Click a category to explore projects.
      filters:
        folders:
          - projects
        exclude_children: true   # 👈 prevents showing nested projects
    design:
      view: article-grid
      fill_image: false
      columns: 2
      show_date: false
      show_read_time: false
      show_read_more: true
---
