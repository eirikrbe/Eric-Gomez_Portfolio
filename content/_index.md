---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-01-05
type: landing

sections:
  # Developer Hero - Gradient background with name, role, social, and CTAs
  - block: dev-hero
    id: hero
    content:
      username: me
      avatar: /assets/media/authors/eric-gomez.jpg
      greeting: "Hi, I'm"
      show_status: true
      show_scroll_indicator: true
      typewriter:
        enable: true
        prefix: "I build"
        strings:
          - "reliable software for telecoms"
          - "data-driven tools"
          - "testable Python services"
          - "RF optimisation tools"
        type_speed: 70
        delete_speed: 40
        pause_time: 2500
      cta_buttons:
        - text: View My Work
          url: "#projects"
          icon: arrow-down
        - text: Get In Touch
          url: "#contact"
          icon: envelope
    design:
      style: centered
      avatar_shape: circle
      animations: true
      background:
        color:
          light: "#fafafa"
          dark: "#0a0a0f"
      spacing:
        padding: ["6rem", "0", "4rem", "0"]
  
  # Filterable Portfolio - Alpine.js powered project filtering
  - block: portfolio
    id: projects
    content:
      title: "Featured Projects"
      subtitle: "A selection of my recent work"
      count: 0
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
        - name: Full-Stack
          tag: Full-Stack
        - name: Frontend
          tag: Frontend
        - name: Backend
          tag: Backend
      default_button_index: 0
      # Archive link auto-shown if more projects exist than 'count' above
      # archive:
      #   enable: false  # Set to false to explicitly hide
      #   text: "Browse All"  # Customize text
      #   link: "/work/"  # Custom URL
    design:
      columns: 3
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Visual Tech Stack - Icons organized by category
  - block: tech-stack
    id: skills
    content:
      title: "Tech Stack"
      subtitle: "Technologies I use to build things"
      categories:
        - name: Languages
          items:
            - name: Python
              icon: devicon/python
            - name: C / C++
              icon: devicon/cplusplus
            - name: SQL
              icon: devicon/postgresql
            - name: MATLAB
              icon: devicon/matlab
        - name: Web & Backend
          items:
            - name: Flask
              icon: devicon/python
            - name: PostgreSQL
              icon: devicon/postgresql
            - name: SQLite
              icon: devicon/sqlite
            - name: psycopg3
              icon: brands/python
        - name: Telecom & Tools
          items:
            - name: RF optimisation
              icon: solid/signal
            - name: NetAct
              icon: solid/server
            - name: PuTTY
              icon: solid/terminal
            - name: KPI analysis
              icon: solid/chart-line
        - name: DevOps & Office
          items:
            - name: Docker
              icon: devicon/docker
            - name: Git
              icon: brands/github
            - name: Excel
              icon: brands/microsoft
            - name: Google Workspace
              icon: brands/google
    design:
      style: grid
      show_levels: false
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Experience Timeline
  - block: resume-experience
    id: experience
    content:
      title: Experience
      date_format: Jan 2006
      items:
        - title: Quality Assurance Engineer
          company: Claro (Colombia)
          company_url: ''
          company_logo: ''
          location: Colombia
          date_start: '2019-10-01'
          date_end: '2022-11-30'
          description: |2-
            * Coordinated quality assurance for mobile network projects across Nokia, Ericsson and Huawei
            * Designed and executed test cases in test and production environments
            * Investigated faults, analysed network data and produced operational reports
        - title: Network Engineer
          company: Nokia Networks (Colombia)
          company_url: ''
          company_logo: ''
          location: Colombia
          date_start: '2017-03-01'
          date_end: '2019-10-01'
          description: |2-
            * Roles included QA-NOC Engineer, RF Junior Engineer, and RAN Back Office Engineer
            * Monitored GSM, UMTS and LTE network performance and KPIs
            * Supported LTE second-carrier projects and RF optimisation tasks
        - title: Duty Manager
          company: Cāntīng by Nic Watt, Auckland
          company_url: ''
          company_logo: ''
          location: Auckland, NZ
          date_start: '2025-08-01'
          date_end: '2026-06-01'
          description: |2-
            * LCQ-certified licence controller; ran shifts, performed cash reconciliation and end-of-day reporting
        - title: Front of House
          company: CBK, Rotorua
          company_url: ''
          company_logo: ''
          location: Rotorua, NZ
          date_start: '2023-06-01'
          date_end: '2025-06-01'
          description: |2-
            * Server, barman and barista duties; trained new staff and managed service sections during peak periods
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Recent Blog Posts
  - block: collection
    id: blog
    content:
      title: Recent Posts
      subtitle: 'Thoughts on web development, tech, and more'
      text: ''
      filters:
        folders:
          - blog
        exclude_featured: false
      count: 3
      order: desc
    design:
      view: card
      columns: 3
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Contact Section
  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Let's build something amazing together"
      text: |-
        I'm always interested in hearing about new projects and opportunities.
        Whether you're looking to hire, collaborate, or just want to say hi, feel free to reach out!
      email: ericfabian10@gmail.com
      autolink: true
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # CTA Card
  - block: cta-card
    content:
      title: "Open to Opportunities"
      text: |-
        I'm currently looking for **senior engineering** or **tech lead** roles.
        
        Let's connect and discuss how I can help your team.
      button:
        text: 'Download Resume'
        url: uploads/resume.pdf
        new_tab: true
    design:
      card:
        # Light mode: soft pastel theme gradient | Dark mode: rich deep gradient
        css_class: 'bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700'
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---
