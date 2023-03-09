---
categories: ["epigenetics", "clocks", "mitosis", "demethylation", "PMD", "DNA replication", "DNA methylation"]
date: November 8, 2022
date-modified: November 18, 2022
doi: 10.1038/s41467-022-34268-8
---

## Cell division drives DNA methylation loss in late-replicating domains in primary human cells {.unnumbered}

> Endicott JL, Nolte PA, Shen H, Laird PW. Cell division drives DNA methylation
> loss in late-replicating domains in primary human cells. Nat Commun. 2022 Nov
> 8;13(1):6659. doi: 10.1038/s41467-022-34268-8. PMID:
> [36347867](https://pubmed.ncbi.nlm.nih.gov/36347867/); PMCID: PMC9643452.

[Nature Communications](https://doi.org/10.1038/s41467-022-34268-8)

[Zhou et al.](dna_methylation_loss_late_replicating_domains_linked_mitotic_cell_division.md)
showed that there is a loss of DNA methylation at certain regions of the genome
that they suggested was caused by mitosis. This paper experimentally shows that
this loss is driven by cellular division independent of time. Methylation loss
is negatively correlated with population doubling in a cell culture. It occurs
more at solo-WGCWs, lone CG dinucleotides within a 35-bp region flanked by A or
T nucleotides, than at social WGCWs. The loss is greater at regions that
replcate late than earlier replication regions, which they believe is indicative
of poor maintenance methylation and possibly chromatin inaccessibility. Most
domains with solo-WGCWs are gene-poor, but those with highly expressed genes had
lower rates of methylation loss in a cell-type specific manner. Stopping DNA
replication stops the methylation loss. Ambient oxygen concentrations for cell
culture lead to increased rates of methylation loss.

Using the collected methylation data, they build a model using elastic net
regression to predict relative mitotic history. It performed better than other
existing methods that were trained on comparisons between different time points,
unlike this model which is based on measured cell divisions. It is however, best
suited to single cell type populations since it was trained on homogeneious
primary cell culture.
