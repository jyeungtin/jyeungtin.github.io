---
layout: page
title: migration-trade-terrorism network analysis
description: A temporal, multiplex network analysis
img: https://news.bbcimg.co.uk/media/images/83295000/gif/_83295879_big_arrows_world_map_labels2.gif
importance: 1
category: Conference
---

## Project summary
Migration, trade and terrorism networks are centre to research efforts in the past decades and each of them have received a considerable amount of attention in their specific domains. However, little work has been done to understand the dynamics between these networks, particularly how temporal growth of one network may induce shocks in another. In this work, we examine how we can leverage techniques in multiplex, temporal networks to disentangle global trends of migration, trade and terrorism from 1990 to 2020. 

### Collaborators 

This is a proud collaboration between my amazing classmates [Tedi Yankov](https://www.oii.ox.ac.uk/people/profiles/teodor-yankov/) and [Sinclaire Schuetze](https://www.oii.ox.ac.uk/people/profiles/sinclaire-schuetze/). 

### Software

Python, Teneto, NetworkX

## Current progress

You can find the project page on [GitHub](https://github.com/jyeungtin/ParallelNetworkChange).

We are accepted at the [Networks and Time II Conference](https://monmeetings.org/time_net2/) in London! 

### Implementation distance metrics

We are continuously implementing distance metrics to compare structural changes across time and datasets. Currently, we are the following metrics:

1. Spanning Tree distance
2. Centrality-basesd distance
3. Hamming distance
4. Jaccard distance
5. Polynomial distance
6. Ipsen-Mikhailov distance

### Curating datasets

While my collaborators are working on their respective datasets on refugee migration and global trade networks, I am annotating data from the Global Terrorism Database (GTD). Our dataset is currently between 1990 and 2020, but we may expand it in the future. 