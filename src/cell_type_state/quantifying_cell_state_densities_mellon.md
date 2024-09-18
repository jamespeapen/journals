---
categories: ["cell-type vs cell-state", "modelling", "systems biology"]
date: June 18, 2024
date-modified: September 18, 2024
doi: 10.1038/s41592-024-02302-w
---

# Quantifying cell-state densities in single-cell phenotypic landscapes using Mellon

[Nature Methods](https://www.nature.com/articles/s41592-024-02302-w)

> Otto DJ, Jordan C, Dury B, Dien C, Setty M. Quantifying cell-state densities
> in single-cell phenotypic landscapes using Mellon. Nat Methods. 2024
> Jul;21(7):1185-1195. doi: 10.1038/s41592-024-02302-w. Epub 2024 Jun 18. PMID:
> [38890426](https://pubmed.ncbi.nlm.nih.gov/38890426).

This is the first paper I've come across that defines a cell state as a "a
high-dimensional vector of quantitative metrics representing the current
biological makeup of the cell". This is the closest to the idea that a state is
individual to a cell and can be described by what can be measured from that
cell. They use diffusion maps to get interpretable distances between cells and
their neighbors and then, based on these distances, infer densities. High
densities have short distances between neighbors while low densities have
larger neighbor distances. States with rapid transcriptional dynamics have low
densities and tend to be transitional. These rare transitory cells arrive as a
result of enhancer priming and activation of master regulators and "confer
lineage identity." Low density regions seem to be a "hallmark of cell-fate
specification in hematopoesis." Along these fate-specification points, linage
identity genes are unregulated while stem-cell genes are downregulated.

They also are able to place cells on a time-axis continuously as "a cell state
present in preceding and following timepoints is likely to exist in the current
time point, even if it has not been directly observed".

Mellon can work with scRNA-seq, scATAC-seq and single-cell histone data. For
ATAC data they did use SEACells to find the metacells to overcome the data
sparsity and examine cells at the metacell resolution instead of single-cell
resolution.

