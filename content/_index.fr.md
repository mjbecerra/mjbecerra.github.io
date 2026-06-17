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
        text: Télécharger CV
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
      title: 'Mes Recherches'
      subtitle: ''
      text: |-
        Mon travail se situe à l'intersection de la géographie critique, des études autochtones et des sciences de l'environnement. J'utilise les SIG, la cartographie participative et des méthodes mixtes pour étudier comment les peuples autochtones font face au changement climatique, aux droits territoriaux et aux pressions socio-environnementales en Amazonie et en Amérique latine côtière.

        Je m'intéresse particulièrement aux dimensions spatiales de la perception du changement climatique, à la gouvernance des territoires autochtones et au rôle de l'éducation environnementale dans le renforcement de la résilience communautaire.

        Je suis ouvert à la collaboration avec des chercheurs travaillant sur la durabilité amazonienne, la cartographie autochtone et la géographie critique. N'hésitez pas à me contacter.
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Publications Phares
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: Publications Récentes
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---
