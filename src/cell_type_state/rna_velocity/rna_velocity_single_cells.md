---
categories: ["rna velocity", "cell-type vs cell-state", "single-cell", "transcriptomics"]
date: August 8, 2018
date-modified: May 25, 2022
doi: 10.1038/s41586-018-0414-6
---

# RNA velocity of single cells {.unnumbered}

[Nature](https://www.nature.com/articles/s41586-018-0414-6/)

> La Manno G, Soldatov R, Zeisel A, Braun E, Hochgerner H, Petukhov V,
> Lidschreiber K, Kastriti ME, Lönnerberg P, Furlan A, Fan J, Borm LE, Liu Z,
> van Bruggen D, Guo J, He X, Barker R, Sundström E, Castelo-Branco G, Cramer P,
> Adameyko I, Linnarsson S, Kharchenko PV. RNA velocity of single cells. Nature.
> 2018 Aug;560(7719):494-498. doi: 10.1038/s41586-018-0414-6. Epub 2018 Aug 8.
> PMID: [30089906](https://pubmed.ncbi.nlm.nih.gov/30089906/); PMCID: PMC6130801.

RNA abundance is an indicator of cell state and single-cell RNA sequencing can be
used to capture cell-level RNA levels. To go beyond the static picture that RNA
sequencing provides, distinguishing unspliced and spliced mRNAs can be used to
predict a future cell state.

mRNA introns are spliced out after transcription to form spliced mRNA which is
then degraded. The change in spliced mRNA can be modelled as 

$$ \frac{ds}{dt} = u - \gamma s $$

where 

- $u$ is the unspliced mRNA,

- $\gamma$ is the spliced mRNA degradation rate, and 

- $s$ is the spliced mRNA.

The quantity of spliced mRNA at a certain timepoint is *correlated
with*[![](https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fs41586-018-0414-6/MediaObjects/41586_2018_414_Fig1_HTML.png?as=webp)]{.aside}
and can be predictive of the quantity of unspliced mRNA at the next timepoint.
Knowing how much unspliced mRNA there is for a gene at one point means we can
predict whether that gene is actively expressed or was previously expressed and
will not be expressed in the future. Coupled with information on genes that
define cell states and types, we can show the trajectory a cell will take in the
near future. RNA velocity allows us to understand what the origin of different
cell types and states are before we have information about the developmental
process [![](https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fs41586-018-0414-6/MediaObjects/41586_2018_414_Fig3_HTML.png?as=webp)]{.aside}.

Computed velocities can be projected onto low dimensional embeddings of data
like a PCA to visualise the trajectories between different cell states. However,
since they are low dimensional, the trajectories may not be fully representative
and would need examination in different dimensional combinations (eg: PC2 vs
PC3). 

