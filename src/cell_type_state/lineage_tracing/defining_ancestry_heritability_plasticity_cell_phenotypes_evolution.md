---
categories: ["lineage tracing", "scRNA-seq", "modelling", "evolution"]
date: December 30, 2022
date-modified: Jan 04, 2023
---

# Defining ancestry, heritability and plasticity of cellular phenotypes in somatic evolution {.unnumbered}

[BioRχiv](https://www.biorxiv.org/content/10.1101/2022.12.28.522128v1)

Although all cells in a multicellular organism come from a single-cell and have
the same genetic information, they can still be phenotypically diverse. This
diversity can be maintained through cell-intrinsic factors like epigenetic
modifications and extrinsic factors like cellular microenvironment. At each
division changes can be introduced that affect the cells phenotype in a highly
context-dependent way - mutations that increase proliferative potential don't
become tumors in progenitor cells.

Single-cell data can be used to trace cell lineage both using artificial
and native lineage markers. The native markers include copy number changes,
single nucleotide mutations and epigenetic patterns. With scRNA-seq we get
transcriptional states and with lineage tracing we get a tree to place the
states on. Neither the trees nor the transcriptional data on their own show how
stable or plastic a certain state is, which is necessary to understand somatic
cell evolution.

Existing lineage tracing data that can be used to create phylogenetic trees can
analysed to quantify heritability and plasticity of somatic phenotypes like a
cells transcriptional state. The PATH tool from this paper can infer cell state
how heritable or plastic a cell state's phenotype is and use that measure to
infer cell state transition dynamics. PATH takes phylogenetic signals and
measures the correlations between phenotypes to tell whether a state is plastic
or heritable.

PATH's "phylogenetic auto-correlation measures how much phenotypic resemblance
close relatives have to one another compared to randomly chosen cells. If cells
resemble close relatives much more than randomly chosen cells, the phenotype
will appear highly heritable and phylogenetically auto-correlated. ..phylogenetic
auto-correlation captures the temporal stability or transience of a cell state".

The tools is affected by sample size and incomplete sampling can lead to
overestimations of relatedness making cell states seem closer than they really
are. Phylogenies without branch length information can also affect inference
quality.
