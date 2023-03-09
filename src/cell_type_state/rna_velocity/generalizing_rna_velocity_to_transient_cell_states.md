---
categories: ["rna velocity", "cell-type vs cell-state", "single-cell", "transcriptomics"]
date: August 3, 2022
date-modified: May 25, 2022
doi: 10.1038/s41587-020-0591-3
---

# Generalizing RNA velocity to transient cell states through dynamical modeling {.unnumbered}

> Bergen V, Lange M, Peidli S, Wolf FA, Theis FJ. Generalizing RNA velocity to
> transient cell states through dynamical modeling. Nat Biotechnol. 2020
> Dec;38(12):1408-1414. doi: 10.1038/s41587-020-0591-3. Epub 2020 Aug 3. PMID:
> [32747759](https://pubmed.ncbi.nlm.nih.gov/32747759/).

[Nature biotechnology](https://www.nature.com/articles/s41587-020-0591-3)

RNA velocity is the change in mRNA abundance. This depends on the ratio between
spliced and unspliced mRNA and the assumption that they reach a steady-state.
Velocities are determined as the deviation of the observed ratio from the
steady-state ratio. This depends on the gene-level capture of the full splicing
dynamics with transcriptional induction, repression and steady-state mRNA
levels and on all genes sharing a common splicing rate. While RNA velocity
prediction allows us to see how cells change their state, the base algorithm
does not do well when the assumptions of a common splicing rate or having the
full splicing dynamics are violated. Further, not all experiments are done in a
time-frame that involves reaching the steady-state.

scVelo uses a likelihood-based dynamical model rather than a steady-state model
that solves the problems with those assumptions. It works by generalizing RNA
velocity estimation to transient systems and systems whose subpopulation
kinetics are heterogeneous. They can infer gene-specific reaction rates of
transcription, splicing and degradation. They can also infer the underlying
gene-shared latent time which represents the cell's internal clock that
describes the cell's position in the underlying biological processes. This is
different from existing pseudotime methods because it is based only on
transcriptional dynamics and takes both speed and direction into account.
Dynamical modelling allows for delineating cell cycling, lineage commitment,
cell cycle exit and endocrine differentiation. This method, however, still
assumes constant reaction rate and is limited by alternative splicing.
