---
title: ''
date: 2022-10-24
type: landing

design:
  spacing: '6rem'

sections:
  # Bio + photo + CV
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

  # Education card
  - block: resume-education
    content:
      title: Education
      username: admin
    design:
      view: card
      columns: 2

  # Skills card
  - block: resume-skills
    content:
      title: Skills
      username: admin
    design:
      view: card
      columns: 2

  # Languages card
  - block: resume-languages
    content:
      title: Languages
      username: admin
    design:
      view: card
      columns: 2

  # Awards & Certifications
  - block: resume-awards
    content:
      title: Awards & Certifications
      username: admin
    design:
      view: card
      columns: 2
---
