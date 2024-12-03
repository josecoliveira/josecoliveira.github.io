---
title: Quantitative Models for Social Networks
authors:
  - josecoliveira

date: '2024-08-30'
publication_type: ['thesis']

publication: University of Minnesota

abstract: Recently, social networks have begun to influence every aspect of our lives, with unprecedented, unanticipated consequences, especially in politics and public opinion. Research on social networks has studied opinions and their change over time, but to accurately model real people and their opinions and beliefs, we must include representations of uncertainty and inconsistency in formal models of social networks. This work presents models for social networks that includes representation of uncertainty, inconsistencies and dynamic trust between agents.We developed a model for social networks using subjective logic, a probabilistic multi-agent logic with operations like trust-discount and belief fusion. We devise a desiderata of properties for an opinoin update function and explore update function with these operations. We found that no function with these operators satisfies our desiderata, but a function using cumulative belief fusion can represent interactions that can lead to polarization.We expand the Alvim-Knight-Valencia model for social networks with dynamic influence allowing belief update function to change the influence over time. Using results from previous works in the AKV model, we define balance-conservative graphs, graphs where agents influence and are influenced by the same degree for every timestep. We conjecture that if there are two agents in a balanced graph that have different total influence, then the graph is not balanced-conservative.Finally, we develop two Python tools for modeling and simulation with the AKV model and the Paraconsistent Gödel Modal Logic, a logic to reason about uncertainty and inconsistency. Using the AKV tool, we reproduced the results from previous works in the model. These tools are available publicly and under the MIT license, allowing researchers to freely use it and contribute.

featured: true

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

image:
  caption: ''
  focal_point: ''
  preview_only: false

share: false
---