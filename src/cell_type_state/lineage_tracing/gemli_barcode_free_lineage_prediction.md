---
categories: ["lineage tracing", "scRNA-seq", "transcriptomics"]
date: September 20, 2022
date-modified: Nov 21, 2022
---

# Barcode-free prediction of cell lineages from scRNA-seq datasets {.unnumbered}

[BioRχiv](https://www.biorxiv.org/content/10.1101/2022.09.20.508646v1.full)

While most scRNA-seq methods need cellular barcoding for lineage tracing, this
paper uses standard scRNA-sequencing methods and finds genes that maintain their
expression level over cell divisions. Barcoding can be technically complex and
require specialized devices. They came up with the concept of 'memory' genes
that are highly conserved across cell types and are on a high expression mean or
have high variability. They were defined as genes with high variability in mean
expression across cell lineages than across random samples. Analysis of the
overlaps between the identified memory genes suggested that a "subset of memory
gene drives overall similarity of cell lineages." They developed GEMLI which can
identify these memory genes and use them to perform hierarchical clustering for
lineage inference. GEMLI is suited for time spans of a few cell divisions over
the course of a few days. This lies between methods like RNA velocity which is
highly dynamic and methods like lineage inference from SNPs or CNVs that require
a long time.

GEMLI works best with high sequencing depth, but does well enough between 5,000
to 8,000 reads/cell. It is also limited by datasets where only a small portion
of populations get sequenced.
