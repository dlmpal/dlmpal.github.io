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
        url: uploads/cv.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          filename: amr.png
          filters:
            brightness: 0.6
          size: cover
          position: center
          parallax: false
  - block: markdown
    content:
      title: 'Software'
      subtitle: ''
      text: |
        I enjoy developing numerical software, such as finite-element and finite-volume solvers. Some examples:
        
        -[SFEM](/sfem): A parallel C++ framework for the numerical solution of PDEs on unstructured meshes

        -[WELDSIM](/weldsim): Thermal simulation of arc welding with AMR 

        -[mSense](/msense):  A Python framework for Multidisciplinary Analysis and Optimization 

        -[ArgParse](https://github.com/dlmpal/argparse): Lightweight parser for command-line arguments in modern C++

    design:
      columns: '1'
---
