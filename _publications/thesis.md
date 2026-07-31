---
title: "Quantitative Models for Social Networks"
date: 2024-08-01
authors: "José Carlos De Oliveira"
venue: "MS Thesis, University of Minnesota (2024)"
pdf_url: "https://www.dropbox.com/scl/fi/rg9krjcv3rthzzi0lue98/Jos-C.-Oliveira-Quantitative-Models-for-Social-Networks.pdf?rlkey=rnn94lv4avmr0cumtcnqjuq7j&st=4doj3qj3&dl=0"
---

**José Carlos De Oliveira**

*MS Thesis, University of Minnesota, August 2024*

[PDF]({{ page.pdf_url }}) \| [Cite](/assets/bib/thesis.bib) \| [Back to Publications](/publications/)

## Abstract

Recently, social networks have begun to influence every aspect of our lives, with unprecedented, unanticipated consequences, especially in politics and public opinion. Research on social networks has studied opinions and their change over time, but to accurately model real people and their opinions and beliefs, we must include representations of uncertainty and inconsistency in formal models of social networks.

This work presents models for social networks that includes representation of uncertainty, inconsistencies and dynamic trust between agents. We developed a model for social networks using subjective logic, a probabilistic multi-agent logic with operations like trust-discount and belief fusion. We devise a desiderata of properties for an opinion update function and explore update functions with these operations. We found that no function with these operators satisfies our desiderata, but a function using cumulative belief fusion can represent interactions that can lead to polarization.

We expand the Alvim-Knight-Valencia model for social networks with dynamic influence allowing belief update function to change the influence over time. Using results from previous works in the AKV model, we define balance-conservative graphs, graphs where agents influence and are influenced by the same degree for every timestep. We conjecture that if there are two agents in a balanced graph that have different total influence, then the graph is not balanced-conservative.

Finally, we develop two Python tools for modeling and simulation with the AKV model and the Paraconsistent Gödel Modal Logic, a logic to reason about uncertainty and inconsistency. Using the AKV tool, we reproduced the results from previous works in the model. These tools are available publicly and under the MIT license, allowing researchers to freely use it and contribute.


