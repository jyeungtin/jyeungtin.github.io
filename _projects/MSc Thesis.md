---
layout: page
title: Covert network robustness
description: MSc thesis project
img: https://www.tandfonline.com/cms/asset/96c455be-4d5e-47c6-b371-fed5c2bd9aa9/ftpv_a_1586675_f0002_oc.jpg
importance: 1
category: Study
---

## Project summary
Graph robustness is extremely important in various contexts. For example, urban designers would want to devise better land use planning to make sure the network of power grids are resilient against (cascading) failures when under attack. At the same time, we are interested in understanding how we can more efficiently attack a covert and illicit network such as drug trades and money laundering ones.

My thesis highlights this specific subfield of network science, generally called graph robustness and related to the theory of security-efficiency trade-off. Particularly, I am interested in exploring (1) new ways to attack networks, (2) new proxies of security and efficiency, (3) dynamic network and (4) the graph incompleteness problem. These are broad, and potentially very difficult questions to answer. Nonetheless, with my thesis, I aim to shed some light on these intriguing questions.

### Supervisor 

My thesis is conducted under the Oxford Internet Institute and supervised by Prof. Renaud Lambiotte at the Oxford Mathematics Institute. 

### Software

Python, NetworkX, Teneto, Numpy

## Current progress 

### Structural changes of covert networks

Existing literature on the growth of individual terrorist networks have uncovered important features of the evolutions of these covert organizations. According McMillan et al. (2020), terrorist networks tend to engage in two (conventional) network growth mechanism, namely preferential attachment and triadic formation. Interestingly, to balance both security and efficiency of communication within the network, terrorists organization tend *not* to create redundant paths in the network (i.e., transitivity), as well as to avoid concentration on a given person (i.e., preferential attachment). However, this preference changes prior the attack taking place. Thus, we can understand that this growing mechanism as a time-variant extension of BA-HK where the probability of preferential attachment and triadic formation is dependent on the time before the attack. The expectation of this time-variant pertubation model is that, although preferential attachment and triadic formation are still driving the growth of the model, the probability grow, perhaps linearly, with time elapsed from time point. 

Using three empirical networks, I mapped out how degree centralization and transitivity (as measured by average clustering coefficient) over time.

