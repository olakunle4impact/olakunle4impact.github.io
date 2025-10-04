---
# Leave the homepage title empty to use the site title
title: ''
date: 2025-10-02
type: landing
image:
  filename: "media/logo.png"

design:
  # Default section spacing
  spacing: '3rem'

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
        about: ''
        education: ''
        interests: ''
    design:
      # Apply a gradient background
      css_class: hbx-bg-gradient
      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: markdown
    content:
      title: '📚 My Research'
      subtitle: ''
      text: |-
        <div style="text-align: justify; width: 100%; max-width: 100%;">
        My research interests lie at the intersection of forest biometrics, remote sensing, and statistical modeling, with a focus on advancing sustainable forest management and addressing pressing environmental challenges. I am passionate about applying cutting-edge tools such as machine learning, spatial analysis, and GIS to monitor, model, and predict forest dynamics. By integrating statistical approaches with remote sensing data, I seek to generate insights that can guide forest management decisions, improve ecological monitoring, and support climate change mitigation strategies.

        Specifically, my work explores areas such as forest measurements and growth modeling, carbon farming, carbon sequestration, and forest ecology. I am particularly interested in how quantitative methods and geospatial technologies can be used to assess forest productivity, evaluate ecosystem services, and design management practices that balance ecological sustainability with economic needs. My goal is to contribute research that not only advances scientific understanding but also provides practical solutions for managing forests in a changing climate.
    
        Please reach out to collaborate 😃
        </div>

    design:
      columns: '1'
    spacing:
      padding: [0, 0, 0, 0]
    full_width: true
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - events
    design:
      view: card
  - block: collection
    id: news
    content:
      title: Blog Posts
      subtitle: ''
      text: ''
      # Page type to display. E.g. post, talk, publication...
      page_type: blog
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: card
      # Reduce spacing
      spacing:
        padding: [0, 0, 0, 0]

---
