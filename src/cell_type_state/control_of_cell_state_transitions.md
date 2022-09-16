---
categories: ["cell-type vs cell-state", "modelling", "systems biology"]
date: September 15, 2022
---

# RNA velocity of single cells {.unnumbered}

[Nature](https://www.nature.com/articles/s41586-022-05194-y)

September 14, 2022

> Rukhlenko OS, Halasz M, Rauch N, Zhernovkov V, Prince T, Wynne K, Maher S,
> Kashdan E, MacLeod K, Carragher NO, Kolch W, Kholodenko BN. Control of cell
> state transitions. Nature. 2022 Sep 14. doi: 10.1038/s41586-022-05194-y. Epub
> ahead of print. PMID: [36104561](https://pubmed.ncbi.nlm.nih.gov/36104561/).

This paper sets up a system to separate cell states given an omics dataset that
reflects different cell states. Their goal is to understand how a ball rolls
down Waddington's landscape as well as why steering it in a direction works to
push it towards a different cell state. 

It works by first clustering the data with a Support Vector Machine (SVM) that
generates a hyperplane that uses learned molecular characteristics to separate
the cell types. This is used to make a state transition vector that describes
the path from one cell state region to the other. It identifies the molecular
factors that control cell state transitions. They also make a dynamic phenotype
descriptor that quantifies the phenotypic changes a perturbation causes in a
cell and shows the direction in which that perturbation moves the cell - towards
or away from the separating hyperplane. They also have a Bayesian formulation of
modular response analysis that can reconstruct the casual connections between
the network components shown to be part of the transition vector. All these can
be used to understand what changes and how much change is necessary to convert a
cell's state. 

The model's predictions were validated on an experimental model testing cell
states differences and perturbations.
