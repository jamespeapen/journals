---
categories: ["transcriptomics", "scRNA-seq", "bioinformatics", "modelling"]
date: May 24, 2021
date-modified: May 10, 2024
doi: 10.1038/s41588-021-00873-4
---

# Separating measurement and expression models clarifies confusion in single-cell RNA sequencing analysis {.unnumbered}

[Nature Genetics](https://www.nature.com/articles/s41588-021-00873-4)

> Sarkar A, Stephens M. Separating measurement and expression models clarifies
> confusion in single-cell RNA sequencing analysis. Nat Genet. 2021
> Jun;53(6):770-777. doi: 10.1038/s41588-021-00873-4. Epub 2021 May 24. PMID:
> [34031584](https://pubmed.ncbi.nlm.nih.gov/34031584); PMCID: PMC8370014.

scRNA-seq studies use poorly-defined terms like dropout, missing data,
imputation and ,zero inflation that lead to confusion during analysis and
interpretation. This study proposes that the observed data be considered as
reflecting both the true gene expression levels and the measurement error and
that method should start with a simple Poisson model and add complexity as
necessary instead of starting with a complex model.

## Problematic Terms

"**Dropout**" refers to the failure to measure a gene and lead to some genes
showing higher measured expression in some cells than others. However this is
inconsistently used in publications and may refer to observed zeroes, undetected
but expressed zeroes, or undetected molecules. There is no period during a
scRNA-seq experiment where the data is left unobserved, so any zeroes are 0s -
noisy zeroes that are as noisy as any other observation. The use of dropout and
"**missing data**" to refer to observed zeroes leads to "**imputation**" methods
that attempt to fill in those zeroes. Since zeroes are not "missing", the
imputed values are specious.

**Zero-inflated models** are used to deal with the "extra zeroes" in scRNA-seq
data by accounting for the extra zeroes as being inflated by some process.
However there is little evidence to support their use. A process that somehow
introduces zeroes would suggest a systematic effect that only affects specific
genes from specific cells.

## Modeling scRNA-seq measurement

The Poisson model can be used in both bulk and scRNA-seq data and can account
for the many zeroes in scRNA-seq data. It accounts for the lack of observations
of every molecule in every cell. Zeroes are measurements like any other and need
no special treatment. Observing a zero for a gene suggests that the relative
proportion of that gene in the cell is low.

The use of the Poisson model is dependent on three assumptions, with the first
being the most plausibly violated:

1. in each cell, each RNA molecule is equally likely to be observed

2. each molecule is observed independently

3. only a small proportion of the total available molecules in the cell are
   observed

The Poisson model can be modified with bias terms to account for biased sampling
of molecules. When biases are consistent across cells, the model is robust to
ignoring them. When random biases occur, a negative binomial model could deal
with the additional noise better than a Poisson model. How much overdispersion
to allow for remains an open question. However, most datasets will have a small
measurement overdispersion. They emphasize that the Poisson model is
specifically for the measurement model and not the observation model. 

> The measurement model connects the observed counts to the expression levels
by specifying the conditional distribution of the probability of the observed
counts $X$ given the expression levels $\Lambda$: $p(X|\Lambda)$. An expression
model is a model for the expression levels $p(\Lambda)$.

A more flexible model like a negative binomial or a zero-inflated negative
binomial can capture additional variation. These models derive from a Poisson
measurement model combined with expression models.

Generally the Poisson model fits the data well enough for differential
expression analysis, clustering, and dimension reduction. There are instances
such as long-tailed distributions where genes don't quite fit the models above
and require additional care.
