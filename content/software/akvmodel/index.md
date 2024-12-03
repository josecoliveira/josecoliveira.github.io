---
title: 'josecoliveira/akvmodel: v1.2.3 (Python package)'
authors:
  - josecoliveira
  - Sophia Knight

date: '2024-07-25'
# publication_types: ['software']

doi: 10.5281/zenodo.10695209

summary: A Python Tool for Social Network Simulations in the Alvim-Knight-Valencia Model

featured: true

url_pdf: ''
url_code: 'https://github.com/josecoliveira/akvmodel'
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

Formal models for social networks aim to capture the crucial aspects of the evolution of agents' beliefs over time, as communication occurs in a network. The Alvim-Knight-Valencia (AKV) social network model (2019) works on the dynamics of belief updates using a quantitative spectrum of belief values, and an influence graph representing the relationships between agents. Previous work on the AKV model developed belief update functions representing a range of belief update methods.

This package implements the AKV model and a catalog of its belief updates, initial configurations, and update functions from the literature, creating a general tool that incorporates a wide range of possible approaches to belief updates. In addition, we allow the AKV model to have multiple outcomes (or truth values) for the proposition used in the model. This tool facilitates future research using the AKV model without the need to reimplement it also allowing its reproducibility.

## Usage

```python
import numpy as np
from akvmodel import *

# Create model with 10 agents, mildly polarized initial configuration, faintly communicating influence graph, and confirmation bias belief update.
akvmodel = AKV(
    belief_state=InitialConfigurations.mildly(10),
    influence_graph=InfluenceGraphs.faintly(10),
    update_function=UpdateFunctions.confirmation_bias,
)

# Update the model 100 times
for _ in range(100):
    akvmodel.update()

# Get polarization
p = akvmodel.get_polarization()

# Plot polarization evolution for the first outcome in the domain
plt.plot(p[0])
```

See the package at [GitHub](https://github.com/josecoliveira/akvmodel).
