---
categories: ["bioinformatics", "transcriptome", "epigenetics", "systems biology"]
date: July 24, 2017
date-modified: August 19, 2023
doi: 10.1186/s13059-017-1269-0
---

# MATCHER: manifold alignment reveals correspondence between single cell transcriptome and epigenome dynamics {.unnumbered}

[Genome Biology](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-017-1269-0)

> Welch JD, Hartemink AJ, Prins JF. MATCHER: manifold alignment reveals
> correspondence between single cell transcriptome and epigenome dynamics.
> Genome Biol. 2017 Jul 24;18(1):138. doi: 10.1186/s13059-017-1269-0. PMID:
> [28738873](https://pubmed.ncbi.nlm.nih.gov/28738873); PMCID: PMC5525279.

MATCHER identifies correlations between epigenome and transcriptome dynamics to
reveal the sequential changes cells undergo during biological processes. It
works on both sampling of the transcriptome and epigenome from different cells
and from the same cells. It is based on the hypothesis that

    cells undergoing a common process are sequenced using multiple genomic techniques, examining any of the genomic quantities should reveal the same underlying biological process.

By projecting a low-dimensional representation of each measure on a common
plane, the different measures can be compared. If all the measures from from the
same cell or sampling event, they can be aligned with correspondence. A similar
system can be used to integrate video, audio and written transcripts of a
speech. If not they are aligned using geometric information without
correspondence. MATCHER is designed for alignment without correspondence since
getting multiple measures from a single cell can be difficult.

## Modelling

MATCHER uses a Gaussian process latent variable model (GPLVM), a non-linear
model of high-dimensional data as a function of latent variables to infer a
pseudotime for each measure. A PCA can be considered a linear version of this
model. GPL VMs are also generative and can predict missing observations in one
measure given data at both measures at other points along the manifold.

All these measures are then mapped onto a "master time" between 0 and 1 using a
learned monotonic warping function. This provides a common plane of comparison
between different data measures. This is what allows integrating data even when
the different measures came from different cells instead of the same cell.

### Assumptions

1. The data lie on a 1D manifold.

2. Each measure changes as a response to the same underlying biological
   process.

3. The process flows in one direction without reversals, branches or cycles.

4. They cells are from the same population and cell type.

These assumptions leave orientation (one measure increases while another
decreases), scale and time warping (genomic measures change at different
rates) as the remaining sources of differences between the different measures.
Correct orientation needs an informed prior since it cannot be inferred from
data while scale differences can be addressed by normalizing the manifold
coordinates. Time warping is addressed by learning a monotonic warping function
for each data type. For branching trajectories, each branch could be assigned
cells and aligned separately.

## Analysis

Using simulated data they showed that MATCHER could accurately infer master time
across warping functions and noise levels. With real data of DNA methylation and
gene expression from the same cells, MATCHER could infer master time values that
were highly concordant. It was also able to infer correlations between the
measures that closely matched the true correlations.

Using gene expression, chromatin accessibility and histone modification data,
MATCHER inferred positive correlations, confirming on a single-cell level,
findings from bulk data. Chromatin was being remodeled to prime lineage-specific
genes and shut down pluripotency genes.

Between DNA methylation and gene expression they found that master time tracked
together well until a master time of 0.3 when coupling decreased. Based on
statistical tests on the data, they hypothesized that

    specific *de novo* DNA methylation changes are required to trigger a key step
    in the process of gene expression changes during the transition from ground
    state pluripotency to a primed state, but after this point in the process,
    the sequential gene expression changes proceed somewhat independently from
    the DNA methylation changes.

Examining relative ordering showed that DNA methylation changes lagged behind
gene expression changes. DNA methylation pseudotime was bimodal suggesting that
there were two metastable states that cells could rapidly travel between. Once
the methylation changes required to push cells out of a certain transcriptomic
space, DNA methylation profiles stabilize. The decoupling is only partial - DNA
methylation and gene expression still correlate, but are only somewhat
predictive of each other. This could be because there are other factors that
regulate gene expression. In iPSC reprogramming, there is higher concordance and
both gene expression and methylation master time densities are bimodal. This
does show that getting the individual genomic measures from the same cell
provides information about the system that MATCHER cannot infer. While
individual master times can sometimes be discordant, a shared master time showed
greater correlation when shared data is available to get a shared cell ordering.
