---
categories: ["cell-type vs cell-state", "transcriptomics", "HSC"]
date: May 21, 2008
date-modified: March 20, 2023
doi: 10.1038/nature06965
---

# Transcriptome-wide noise controls lineage choice in mammalian progenitor cells {.unnumbered}

[Nature](http://www.nature.com/articles/nature06965)

> Chang HH, Hemberg M, Barahona M, Ingber DE, Huang S. Transcriptome-wide noise
> controls lineage choice in mammalian progenitor cells. Nature. 2008 May
> 22;453(7194):544-7. doi: 10.1038/nature06965. PMID:
> [18497826](https://pubmed.ncbi.nlm.nih.gov/18497826); PMCID: PMC5546414.

[![](https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fnature06965/MediaObjects/41586_2008_Article_BFnature06965_Fig2_HTML.jpg)]{.aside}
This study examined the transcriptional heterogeneity in a mouse haematopoietic
cell progenitor cell line that expressed the Sca-1 stem cell marker across a
1000-fold range. They separated the cells into three groups based on Sca-1
expression levels as Sca-1$^{high/mid/low}$. All three groups were cultured
separately and their Sca-1 expression levels measured over 9 days. All groups,
despite starting with different initial expression levels, reverted back to the
distribution found in the parental group of mixed cells.


These results could simplistically be modelled using an **Ornstein-Uhlenbeck
process** [A model describing processes that tend towards the mean over
time]{.aside} that models mean-reverting processes, but it did not explain the
long left tail found in the expression data. They extended the
Ornstein-Uhlenbeck model to include the transitions between the cellular
subpopulations with a Gaussian mixture model made of two states. However, this
only accounted for a small part of the process restoring heterogeneity, while
the transitions between the populations had a more important role, demonstrating
that the heterogeneity is not just mean-reverting noise around an attractor, but

> the result of a process involving stochastic state transitions in a system
exhibiting multiple stable states.

Clonal heterogeneity in the cells correlated with the heterogeneity in their
differentiation potentials as the Sca-1$^{low}$ population had the highest
commitment and differentiation rate to the erythroid lineage and Sca-1$^{high}$
had the lowest rates. Despise the faster commitment, the Sca-1$^{low}$ cells
were still undifferentiated, expressing the c-kit stem cell marker, and
maintained their ability to recreate the Sca-1 expression distribution of the
parental population. They were transcriptionally more similar to the
differentiated erythroid cells than the Sca-1$^{high}$ cells were. These
differences in erythroid differentiation rates were lost when the cells were
stimulated to at days 7, 14, and 21 h. Despite all three populations converging
on a similar Sca-1 expression distribution, there was still variation in their
differentiation rates even past 14 days which meant the Sca-1 heterogeneity is
only one dimension controlling differentiation potential.

[![](https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fnature06965/MediaObjects/41586_2008_Article_BFnature06965_Fig3_HTML.jpg)]{.aside}

Other dimensions include the expression of other fate-determining factors like
the transcription factors Gata1 and PU.1, which are mutually repressive. The
Sca-1$^{low}$ group with faster erythroid differentiation had more *Gata1* mRNA
and the Sca-1$^{high}$ group had high expression of *PU.1*. All three groups
were transcriptionally significantly different, but the difference decreased
over time, not only for Sca-1, but over their global gene expression profiles.
Such heterogeneity

> primes the cells for different lineage choices.

The relaxation of differences suggests a model where the progenitor state is a

> high dimensional attractor state.

It is a dynamical system that shows multistability where cells can make discrete
transitions to different states and prime for cell fate commitment. Average
expression may not be a good indicator or determinant of function.
