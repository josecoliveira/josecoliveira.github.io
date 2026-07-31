---
title: "kg2: Paraconsistent Gödel Modal Logic Tool"
date: 2024-07-26
authors: "José C. Oliveira, Sophia Knight"
version: "v1.1.0"
github_url: "https://github.com/josecoliveira/kg2"
doi_url: "https://doi.org/10.5281/zenodo.12855589"
description: "A Python package for model checking in Paraconsistent Gödel Modal Logic, a logic for reasoning about uncertainty and inconsistency where beliefs are represented as pairs of values."
---

**josecoliveira/kg2: {{ page.version }} (Python package)**

**Authors:** {{ page.authors }}

**Date:** July 26, 2024

**Links:** [GitHub]({{ page.github_url }}) \| [DOI]({{ page.doi_url }}) \| [Back to Projects](/projects/)

## Description

This package implements model and evaluation for Paraconsistent Gödel Modal Logic. In this logic, the belief of an agent in a proposition is defined to be a pair of values in the interval $[0, 1]\times[0,1]$, representing the world's truth-value for and against the proposition.

Paraconsistent Gödel Modal Logic is valuable for representing nuanced information about evidence, strength of belief, consistency and inconsistency, and certainty and uncertainty.

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
