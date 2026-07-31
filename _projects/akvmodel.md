---
title: "akvmodel: AKV Social Network Simulator"
date: 2024-07-25
authors: "José C. Oliveira, Sophia Knight"
version: "v1.2.3"
github_url: "https://github.com/josecoliveira/akvmodel"
doi_url: "https://doi.org/10.5281/zenodo.10695209"
description: "A Python package implementing the Alvim-Knight-Valencia (AKV) social network model with a catalog of belief updates, initial configurations, and influence graphs."
---

**josecoliveira/akvmodel: {{ page.version }} (Python package)**

**Authors:** {{ page.authors }}

**Date:** July 25, 2024

**Links:** [GitHub]({{ page.github_url }}) \| [DOI]({{ page.doi_url }}) \| [Back to Projects](/projects/)

## Description

Formal models for social networks aim to capture the crucial aspects of the evolution of agents' beliefs over time, as communication occurs in a network. The Alvim-Knight-Valencia (AKV) social network model (2019) works on the dynamics of belief updates using a quantitative spectrum of belief values, and an influence graph representing the relationships between agents. Previous work on the AKV model developed belief update functions representing a range of belief update methods.

This package implements the AKV model and a catalog of its belief updates, initial configurations, and update functions from the literature, creating a general tool that incorporates a wide range of possible approaches to belief updates. In addition, we allow the AKV model to have multiple outcomes (or truth values) for the proposition used in the model. This tool facilitates future research using the AKV model without the need to reimplement it also allowing its reproducibility.

## Usage

```python
import numpy as np
from akvmodel import *

# Create model with 10 agents, mildly polarized initial configuration,
# faintly communicating influence graph, and confirmation bias belief update.
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
