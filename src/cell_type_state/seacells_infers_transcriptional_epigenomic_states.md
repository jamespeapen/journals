---
categories: ["cell-type vs cell-state", "modelling", "systems biology", "gene regulatory networks", "HSC", "transcriptomics", "ATAC-seq"]
date: March 27, 2023
date-modified: March 30, 2023
doi: 10.1038/s41587-023-01716-9
---

# SEACells infers transcriptional and epigenomic cellular states from single-cell genomics data {.unnumbered}

[Nature Biotechnology](https://www.nature.com/articles/s41587-023-01716-9)

> Persad S, Choo ZN, Dien C, Sohail N, Masilionis I, Chaligné R, Nawy T, Brown
> CC, Sharma R, Peer I, Setty M, Peer D. SEACells infers transcriptional and
> epigenomic cellular states from single-cell genomics data. Nat Biotechnol.
> 2023 Mar 27. doi: 10.1038/s41587-023-01716-9. Epub ahead of print. PMID:
> [36973557](https://pubmed.ncbi.nlm.nih.gov/36973557).

Although single-cell data provides data at high resolution, sparsity, noise and
heterogeneity in the data can make it difficult to analyze the data and draw
conclusions. Each individual cluster can have multiple distinct gene expression
programs with important biological function. This paper uses the metacell
concept to group cell states that are similar as units that can then be used for
analysis. Using metacells instead of individual cells improves the results from
scRNA-seq and scATAC-seq data.

> Metacells are far more granular than clusters and are optimized for
homogeneity within cell groups rather than for separation between clusters.

The SEACells tools identifies metacells across the phenotypic manifold, a lower
dimensional manifold. They use a matrix decomposition method called archetypal
analysis which is usually used to identify the cell states at the boundaries of
the phenotypic space. They use it differently by applying it on a cell-cell
similarity matrix. Metacells work by projecting the data into a higher dimension
where the differences between cells are exaggerated to find the groups of cells
that best make up a discrete and truly similar group:

> two cells are alike only if they share neighbors and the distances to the
> shared neighbors are similar.

These metacells can distinguish states within cell types and capture rare cell
states as well as intermediate cells in low-density regions.

One of the main applications of SEACells is gene regulatory inference from
scATAC-seq data. This is done by identifying transcription factor binding motifs
of accessible chromatin regions from ATAC-seq data. scATAC-seq suffers
from sparsity issues, but SEACells balances resolution with coverage to overcome
sparsity. They found that using only nucleosome-free fragments from the data
performed better than using all fragments at resolving regulatory elements. Gene
regulators are identified by the correlation between accessibility and
expression. Using ATAC metacells captures correlations that were not found at
the single-cell level. SEACells can also model gene accessibility dynamics
during differentiation in the chromatin landscape.

SEACells can also be used to integrate data from multiple sources with
different sources of variation into metacells. They used COVID single-cell data
from different locations and time-points. Batch effects were lower in metacells
than the single-cells. Even a confounding factor turned out to be caused by
differences measurement time along disease-progression showing that SEACells can
preserve biological signal despite technical noise.

Further, since metacells are summarized from single-cell data, using metacells
instead of single-cell's can increase compuational efficiency when large numbers
of cells are involved. They can also be aggregated into metacell aggregates
'meta^2^cells'. In the COVID dataset, this double aggregation was used to
capture both healthy and COVID metacells in combination to show how healthy
cells change in COVID.
