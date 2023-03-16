---
categories: ["transcriptomics", "scRNA-seq", "intro"]
date: June 21, 2021
date-modified: March 16, 2023
doi: 10.1038/s41592-021-01171-x
---

# The triumphs and limitations of computational methods for scRNA-seq {.unnumbered}

[Nature Methods](https://www.nature.com/articles/s41592-021-01171-x)

> Kharchenko PV. The triumphs and limitations of computational methods for
> scRNA-seq. Nat Methods. 2021 Jul;18(7):723-732. doi:
> 10.1038/s41592-021-01171-x. Epub 2021 Jun 21. Erratum in: Nat Methods. 2021
> Jun 30;: PMID: [34155396](https://pubmed.ncbi.nlm.nih.gov/34155396).

Every cell's individual state differs from other cells around it even in the
same tissue and scRNA-seq can capture that variation with high resolution. Even
if mean expression of some genes is similar, there can be biologically
significant variability of expression between cells. That high resolution comes
with some computational challenges that need to be overcome to gain the most
from scRNA-seq data.

Compared to bulk methods, single-cell methods only capture a small number of the
total molecules in a cell with variation between cells reducing the confidence
of expression profiles for some cells compared to others. In addition there is a
gene-specific bias that prevents protocols from getting a random sampling of the
molecules in the cell leading to different transcript-detection rates for
different protocols. We can use more cells to compensate or use computational
methods to infer and impute information. There is also the problem of sparsity:
>missing data could mean the failure to detect a transcript rather than a lack of
that transcript.

Using unique molecular identifiers has reduced the severity of this dropout
problem. Sparsity also changes the way the data and analysis is viewed:

> finding the likelihood that the transcript is expressed at a particular level
given the observed data

For differential expression testing with large populations, parametric tests
do not have a significant advantage over non-parametric tests, but have more
unnecessary assumptions. However, with large populations, more genes will be
reported as differentially expressed and the magnitude of the differences and
the definitions of the subpopulations becomes important in analysis.

With differential expression testing analysis can also include the
quantification of similarity or distance between the cells in the data. Methods
like Euclidean or L1 distances quantify the transcriptional differences between
cells while methods like Poisson similarity or Jensen-Shannon divergence measure
the statistical deviation of two cells from equality and can vary with depth of
coverage. Both types of analysis are subject to the curse of dimensionality
which is the loss of the ability to distinguish between the closest and most
distant points in the data. This requires using a lower dimensional embedding of
the data to calculate distances on.

## Dimensionality reduction

Lower dimensional representations of high dimensional biological data are useful
because most of the variation in the data can be explained using just a few of
the factors of the lower dimensional axes. This also reflects gene expression
programs and the regulatory logic of cells. Although PCA is one of the most
common and interpretable dimensionality reduction tools, the top principal
components focus on the differences of highly expressed transcripts, losing
information about broader expression patterns. One way to deal with this is to
find the expected behaviour from all transcripts and then see if any one shows
further variance above that. This would suggest that its expression pattern
distinguishes major cell subpopulations.

Since PCA works best on symmetrically distributed data (normal distributions),
it is also affected by sparsity and can return technical variation as a top
principal component with high sparsity. These dimensions may need to be
explicitly regressed out. This correction, however, is affected by the fact that
distinct subpopulations can have systematic differences in depth because of
differences in the amounts of mRNA. Instead of normal distributions, count
models like the negative binomial model can better approximate the spread of the
data.

Neural networks can be an easy way to map complex non-linear relationships.
Autoencoders can

> learn a low-dimensional representation of scRNA-seq data by
finding functions that map to and from low-dimensional data in the best way that
allows reconstruction of the original data

Although non-linear methods can capture the underlying structure of the
populations than linear methods, they are significantly harder to interpret.
Linear decoding can be combined with nonlinear encoding using an asymmetric
autoencoder.

## Expression manifolds

An expression manifold is
> a smooth low-dimensional surface on which the observed states of the cells lie
and can be approximated by observing the distributions of the measured cells.

This shape can be represented by neighbor graph representations that usually use
*k*-nearest neighbors to build the network. This graph can then be represented
as a matrix that has a Laplacian. The smallest eigenvalues of the Laplacian's
eigenvectors correspond to the connected components and main structural axes of
the network graph. This approach can derive a low-dimensional representation of
the expression manifold that helps with visualizing the data and analyzing it.

## Clustering cells

A popular clustering approach is to find communities in the data with methods
like Louvain or Leiden clustering. They find clusters of cells that, while
useful for interpretation and differential expression analysis, are not
guaranteed to carry any real meaning. They can capture anything from cell types,
to cell states, to finding differences within a population that is quite
transcriptionally uniform because of weak random variation.

## Dynamic processes

Although scRNA-seq is typically a snapshot of a cell's transcriptional state in
time, there are measures in that snapshot that provide clues to its
transcriptional dynamics. One way to do it is to trace cell density in a
low-dimensional space to elucidate the trajectory cells take in that space. This
requires a dataset with a representation from cells all align that trajectory.
The clustering and dimensionality reduction algorithms specifics behaviours can
affect the results from tracing analyses. It also needs information on the start
and end points to find the path and trace the cells between them.

Another way is to look at the entropy in the data since we know stem or
progenitor cell populations have more heterogeneity than differentiated cells.
Trajectory direction can be assigned in the direction of decreasing entropy.

scRNA-seq also contains information about the RNA structure in terms of
unspliced and spliced RNA. The difference between them can be used to infer what
genes are being turned on and off in a cell population to see what the
underlying trajectories are and what groups cells are moving towards or away
from. This can reveal differentiation trajectories and lineage commitment
points along them.
