---
categories: ["cell-type vs cell-state", "modelling", "systems biology", "gene regulatory networks", "dynamical sytems", "HSC", "transcriptomics"]
date: January 09, 2017
date-modified: March 23, 2023
doi: 10.1371/journal.pbio.2000640
---

# Cell Fate Decision as High-Dimensional Critical State Transition

[PLOS Biology](http://dx.plos.org/10.1371/journal.pbio.2000640)

> Mojtahedi M, Skupin A, Zhou J, Castaño IG, Leong-Quong RY, Chang H, Trachana
> K, Giuliani A, Huang S. Cell Fate Decision as High-Dimensional Critical State
> Transition. PLoS Biol. 2016 Dec 27;14(12):e2000640. doi:
> 10.1371/journal.pbio.2000640. PMID:
> [28027308](https://pubmed.ncbi.nlm.nih.gov/28027308); PMCID: PMC5189937.

Since allows there is
[evidence](transcriptome_wide_noise_controls_lineage_choice.md) for increase in
noise before a lineage choice, this study tried to quantify that noise and see
if such a metric would indicate the point before a fate commitment. They work
with the ESC population that can differentiate into erythroid or myeloid cell
types and see the progenitor and differentiated states as stable attractor
states. Their hypothesis is that differentiation requires creating instability
in the progenitor state. Instability allows the cells to move out of that
attractor basin into the differentiated attractor basins.

In the system of equations for this system

$$ \dot{x}(t) = F(x(t), \mu) $$

$\mu$ is the set of bifurcation parameters that are typically unknown as are the
GRN specifications for cell fate decisions. So instead of trying to formulate a
non-linear dynamical systems model, they use genes they know are components of
the higher dimensional $\boldmath{x}(t)$. These are genes in the regulatory
network of the myeloid/erythroid fates.

They treated the progenitor cells with either erythropoetin or GM-CSF/IL-3 to
push them into the erythroid or myeloid fates. There was also a group that
received both, but these had a longer delay before making a commitment and chose
the myeloid fate, despite the conflicting signals.

With their matrix of *n* cells and *m* genes, they found a decrease in cell-cell
correlation and an increase in gene-gene correlation as differentiation
progressed. Based on these correlations between the cell state vectors and the
genes, they developed an index of critical state transitions, $I_{c}$ that is a
measure of transcriptional noise. It

> measures concomitant changes in cell–cell diversity and gene–gene
> coordination.

Gene correlations increased probably because
the cells go though a narrow saddle point during the move out of the progenitor
attractor. Cell-cell correlation decreased since there is increased instability
and more cell diversity with differentiation. The $I_{c}$ increases as the cells
grow in their growth factors and then drops after differentiation is complete.

> $I_{c}$ captures the information immanent in both the m gene vectors (the
> expression level of a gene across a large number n of individual cells) and
> the n cell vectors.

They validated this in other progenitor cells and showed that the increase is at
the expected time of cell fate commitment.

*m* = 17 for the experiment, so they checked whether increasing that would
affect the $I_{c}$. If most genes considered are not relevant to the cell state
changes, that would make the $I_{c}$ less sensitive. However, since there are
networks regulating gene expression in cells, there may only be a certain range
of possible expression values and this would increase the index sensitivity.
Testing this showed that when more genes are added, the test is more sensitive
and better powered. When the genes are randomly chosen with a more heterogeneous
cell population, sensitivity decreased with the increased noise.

While the differentiation promoting factors for the two lineages pushed the
progenitor population to one or the other, there were some cells in each group
that committed to the opposing lineage. The authors suspect this happened
because these cells were already primed to go in another direction, but when
they receive a contradictory signal they have enough molecular noise to push
them in their primed direction. However, they cannot survive unless they are
provide with the signals that align with their fate choice. External signals and
the internal stochasticity synergize to control cell fate.

When they checked the cells that seemed unresponsive by their lack of change in
the progenitor markers, checking them against a full transcripome and not just
the 17 genes, they saw that these cells had changed. The changes were just not
in the genes they were looking at, but still made them look more like the cells
that did.

The model of selection may be an asymmetric bifurcation. One of the branches is
easier to reach while the other one may be detached and needs more gene
expression noise to be reached. Cell-cell signalling could promote or suppress
directions in the differentiation trajectory, but this study did not examine
them.
