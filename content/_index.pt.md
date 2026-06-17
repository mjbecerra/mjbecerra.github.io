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
        text: Baixar CV
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
      title: 'Minha Pesquisa'
      subtitle: ''
      text: |-
        Meu trabalho situa-se na interseção da geografia crítica, dos estudos indígenas e das ciências ambientais. Utilizo SIG, cartografia participativa e métodos mistos para investigar como os povos indígenas enfrentam as mudanças climáticas, os direitos territoriais e as pressões socioambientais na Amazônia e na América Latina costeira.

        Tenho especial interesse nas dimensões espaciais da percepção das mudanças climáticas, na governança de territórios indígenas e no papel da educação ambiental na construção da resiliência comunitária.

        Estou aberto à colaboração com pesquisadores que trabalhem com sustentabilidade amazônica, cartografia indígena e geografia crítica. Sinta-se à vontade para entrar em contato.
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Publicações em Destaque
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: Publicações Recentes
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---
