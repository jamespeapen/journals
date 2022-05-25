---
categories: ["cell-type vs cell-state", "single-cell", "transcriptomics", "scRNA-seq"]
date: May 24, 2022
---

# The evolving concept of cell identity in the single cell era {.unnumbered}

> Morris SA. The evolving concept of cell identity in the single cell era.
> Development. 2019 Jun 27;146(12):dev169748. doi: 10.1242/dev.169748. PMID:
> [31249002](https://pubmed.ncbi.nlm.nih.gov/31249002/).

[Development](https://journals.biologists.com/dev/article/146/12/dev169748/19444/The-evolving-concept-of-cell-identity-in-the)

June 27, 2019

Cells can exist in a range of phenotypes and expression profiles, within one
cell type. This review introduces a framework to understand cell state and
identity using cell phenotype and function, cell lineage, and cell state. This
allows mapping the landscape of cell states and will allow for a better
understanding of cells that leave the normal landscape and enter diseased
states.

### Phenotype and function

Cell phenotypes like morphology are most commonly and easily used to classify
cells by their morphology and activity. We can also use the transcriptome and
proteome as part of the classification process since these are higher
dimensional and have more features to define cell types. Single-cell
transcriptomic information can provide even more information that bulk studies
to help generate a rigorous and unbiased picture of cell phenotypes. Maintaining
spatial information in single-cell transcriptomics can be a challenge since the
process involves separating the cells, but there are new techniques that allow
for *in situ* visualization of cellular features.

Cell function is an important determinant of cell identity. Cellular function
can be investigated through genetic ablation or or the elimination of cells, but
they have their limitations, especially in humans. However, it is not easy to
understand the function of a new cell type without a large number of assays. In
these situations, gene ontology studies can help provide an idea of the pathways
that cell is involved in based on gene expression patterns. Although this can be
helpful it does not provide a clear definition of cellular function. Proteins
are the effectors of cellular function in cells so they could be used as
predictors of cellular function.

### Cell lineage

If measurements of cellular phenotype yield a new cell type, it is important to
place the new cell type in the context of other cells. This can be achieved by
understanding the cells developmental lineage which would provide clues to
function. Cell lineages and fates can be tracked in a number of different ways.
The tracking data can show an expected lineage or it may show that cells of
different origins end up in a similar fate or that cells from similar embryonic
origins end up at vastly different states.

We can use snRNA-seq data to make temporal reconstructions of lineage. This
results are, however, inferred and would need *in vitro* models of human
development to validate and bolster. Combining lineage data with phenotype and
function data, we can produce a fairly robust picture of cell identity.

### Cell state

Cell state is the "range of cellular phenotypes arising from the interaction of
a defined cell type with its environment". Cells of a certain type can change
their behaviour and expression profile depending on their environment. Cell
identity is generally stable while cell state is more malleable and adjusts,
making just scRNA-seq data insufficient to call a cell type with confidence.
_Epigenetic signatures_[eg: ATAC-seq, methylation data]{.aside}, in combination
with RNA data, can provide more information about chromatic accessibility and
methylation and reveal transcriptional states associated with them.
Technological improvements that allow 'multi-omic' measurements from a
single-cell will allow more robust associations between epigenetic signatures
and transcriptional states. Further, lineage mapping can be applied to cells
with the introduction of perturbations to track the cell's response and its
trajectory through its landscape and will allow us to better understand the
paths that lead to disease states.

