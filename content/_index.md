---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: resume.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to `assets/media/`.
          filename: stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false
  #- block: markdown
  #  content:
  #    title: '📚 My Research'
  #    subtitle: ''
  #    text: |-
  #  design:
  #    columns: '1'
  - block: collection
    id: papers
    content:
      title: Papers
      filters:
        folders:
          - publication
        featured_only: false
    design:
      view: citation
  #- block: collection
  #  content:
  #    title: Preprints
  #    text: ""
  #    filters:
  #      folders:
  #        - preprint
  #      exclude_featured: false
  #  design:
  #    view: citation
  - block: collection
    id: organised
    content:
      title: Organized events
      filters:
        folders:
          - organised
    design:
      view: compact
      columns: 1
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
    design:
      view: compact
      columns: 1
---
