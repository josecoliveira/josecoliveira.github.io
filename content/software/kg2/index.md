---
title: 'josecoliveira/kg2: v1.1.0 (Python package)'
authors:
  - josecoliveira
  - Sophia Knight

date: '2024-07-26'
# publication_types: ['software']

doi: 10.5281/zenodo.12855589

summary: A Python Tool for Paraconsistent Gödel Modal Logic

featured: true

url_pdf: ''
url_code: 'https://github.com/josecoliveira/kg2'
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

This package implements model and evaluation for Paraconsistent Gödel Modal Logic. In this logic, the belief of an agent in a proposition is defined to be a pair of values in the interval {{< math >}}$[0, 1]\times[0,1]${{< /math >}}, representing the world's truth-value for and against the proposition.Paraconsistent Gödel Modal Logic is valuable for representing nuanced information about evidence, strength of belief, consistency and inconsistency, and certainty and uncertainty.

## Usage

```python
from kg2 import *

# Number of worlds in the model.
world_size = 4

# Accessibility relation.
relation = [[1, 1, 0.5, 0.5], [1, 1, 0.5, 0.5], [0.5, 0.5, 1, 1], [0.5, 0.5, 1, 1]]

# Valuation 1 for each variable and agent.
valuation1 = {"p": [1, 1, 0.4, 0.4]}

# Valuation 2 for each variable and agent.
valuation2 = {"p": [0, 0, 0.8, 0.8]}

# Model instantiation.
model = Model(4, relation, valuation1, valuation2)

# Define a formula.
formula = Diamond(Diamond(Variable("p")))

# Evaluate formula in the model for world 0.
formula.valuation1(model, 0)
```

See the package at [GitHub](https://github.com/josecoliveira/kg2).
