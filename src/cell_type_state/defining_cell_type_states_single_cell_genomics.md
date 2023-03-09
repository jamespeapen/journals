---
categories: ["cell-type vs cell-state", "single-cell", "scRNA-seq"]
date: Oct 25, 2015
date-modified: May 23, 2022
doi: 10.1101/gr.190595.115
---

# Defining cell types and states with single-cell genomics {.unnumbered}

> Trapnell C. Defining cell types and states with single-cell genomics. Genome
> Res. 2015 Oct;25(10):1491-8. doi: 10.1101/gr.190595.115. PMID:
> [26430159](https://pubmed.ncbi.nlm.nih.gov/26430159/); PMCID: PMC4579334.

[Genome Research](https://genome.cshlp.org/content/25/10/1491)


### Problems with bulk methods

Bulk methods lose important detail because of averaging that results in the
potential for losing interpretability or making wrong conclusions from the data.
In Simpson's Paradox a group of cells may show a certain gene expression pattern
or correlation. However that pattern can be lost or reversed when they are
grouped by their cell type. Averaging also loses information about cell counts
and can lead to spurious patterns in the data since it does not account for cell
death or divisions. Time series experiments, when averaged, would only show a
mixture of cells rather than a better representation of the expression changes
as the cells differentiate over time.

### Technological advances in cellular state measurement

Most assays require more cell material than is available from a single cell.
This problem has been overcome through advances in amplification methods,
modifications to reverse transcriptase and instrument development to capture
individual cells.

Data analysis in single-cell experiments are significantly more challenging than
bulk experiments since it can be highly variable and hard to distinguish between
technical and biological variation. Some of these problems can be solved by
normalization techniques like spike-ins or molecular barcoding. Further, since
the data is orders of magnitude larger, algorithms need to be particularly
efficient with dealing with that data.

### A dynamical systems view of the cell

Dynamical systems are used to predict complex behaviour and can be used as a
model for cell states and trajectories. As a cell develops and regulates gene
expression, its trajectory shape is a function of its starting position and the
differential equations that dictate changes in its future expression levels
given its current state. 

Distinct cell types can be described as attractors of the system that is a
location that a cell will move toward or return to if disturbed - trajectories
flow towards attractors. These can be used to describe a cell's landscape with
cell fates and paths between them.

### Single-cell clustering and trajectory analysis

Transcriptomic studies show that cells are part of that dynamical landscape and
can be anywhere in it, and are not always in distinct and defined states.
Attractors of such a landscape can be identified through clustering methods like
PCA. These dimensionality reduction techniques can help deal with the "**curse of
dimensionality**"[Distances between points become increasingly similar as the
dimensions of their space increase]{.aside} In biological systems, genes can be
grouped into modules with correlated expression levels allowing one gene to
represent a group, further reducing dimensionality.

Clustering could also be used to understand cell transition paths. Algorithms
like Monocle can cluster cells not only by their type, but also by their
temporal or developmental stage through pseudotime, a measure of biological
progression through a cellular process. This can be done using transcriptomic
data as well as with proteomic data.

### Finding genes that govern a cell state

To identify genes that determine where a cell is on the dynamical landscape, we
need to be able to distinguish between genes differentially expressed during
transitions between states and genes that are 'always on' or constitutively
expressed.

This distinguishing process can be difficult because of the curse of
dimensionality that makes it hard to predict gene-gene interactions and because
averaging loses the source of variation needed to construct gene regulatory
networks.

