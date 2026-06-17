---
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    content:
      username: me
      text: ''
      button:
        text: Descargar CV
        url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle
  - block: markdown
    content:
      title: 'Mi Investigación'
      subtitle: ''
      text: |-
        Mi trabajo se sitúa en la intersección de la geografía crítica, los estudios indígenas y las ciencias ambientales. Utilizo SIG, cartografía participativa y métodos mixtos para investigar cómo los pueblos indígenas se enfrentan al cambio climático, los derechos territoriales y las presiones socioambientales en la Amazonía y América Latina costera.

        Estoy especialmente interesado en las dimensiones espaciales de la percepción del cambio climático, la gobernanza de territorios indígenas y el papel de la educación ambiental en la construcción de resiliencia comunitaria.

        Doy la bienvenida a la colaboración con investigadores que trabajen en sostenibilidad amazónica, cartografía indígena y geografía crítica. No dude en contactarme.
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Publicaciones Destacadas
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: Publicaciones Recientes
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---
