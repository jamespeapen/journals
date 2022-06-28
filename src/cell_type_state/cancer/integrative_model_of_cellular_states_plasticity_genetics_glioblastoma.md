---
categories: ["cell-type vs cell-state", "glioblastoma", "scRNA-seq"]
date: June 28, 2022
---

# An Integrative Model of Cellular States, Plasticity, and Genetics for Glioblastoma {.unnumbered}

> Neftel C, Laffy J, Filbin MG, Hara T, Shore ME, Rahme GJ, Richman AR,
> Silverbush D, Shaw ML, Hebert CM, Dewitt J, Gritsch S, Perez EM, Gonzalez
> Castro LN, Lan X, Druck N, Rodman C, Dionne D, Kaplan A, Bertalan MS, Small J,
> Pelton K, Becker S, Bonal D, Nguyen QD, Servis RL, Fung JM, Mylvaganam R, Mayr
> L, Gojo J, Haberler C, Geyeregger R, Czech T, Slavc I, Nahed BV, Curry WT,
> Carter BS, Wakimoto H, Brastianos PK, Batchelor TT, Stemmer-Rachamimov A,
> Martinez-Lage M, Frosch MP, Stamenkovic I, Riggi N, Rheinbay E, Monje M,
> Rozenblatt-Rosen O, Cahill DP, Patel AP, Hunter T, Verma IM, Ligon KL, Louis
> DN, Regev A, Bernstein BE, Tirosh I, Suvà ML. An Integrative Model of Cellular
> States, Plasticity, and Genetics for Glioblastoma. Cell. 2019 Aug
> 8;178(4):835-849.e21. doi: 10.1016/j.cell.2019.06.024. Epub 2019 Jul 18. PMID:
> [31327527](https://pubmed.ncbi.nlm.nih.gov/31327527/); PMCID: PMC6703186.

[Cell](https://doi.org/10.1016/j.cell.2019.06.024)

August 8, 2019

Glioblastoma tumors show heterogeneity in their subtypes and the genetic
alterations associated with them as well as in the developmental states of the
tumor cells. This occurs through the hijacking of neural development that
maintains glioblastoma stem cells in tumors. Whether different stem cell markers
isolate distinct or similar cell states and whether tumor cells from different
stem cell populations lead to a diverse tumor composition is not known. This
paper uses scRNA-seq to characterize tumor cellular states and understand the
heterogeneity in glioblastoma tumors. 

They saw that malignant cells exist in a set of states that show
neural-progenitor-like (NPC), oligodendrocyte-progenitor-like (OPC),
astrocyte-like (AC), and mesenchymal-like states. The tumors contained the
different types in varying proportions that were associated with _CDK4_,
_PDGFRA_, _EGFR_, and _NF1_. Instead of being a steady-state of the different
types, one or two would be enriched depending on these genes and environmental
factors like chromosomal aberrations. The genetic drivers may drive
the proliferation of particular states leading to heterogeneous tumors driven by
an enriched cell state. Targeting drivers may change the state distribution and
lead to another distribution driving proliferation. This model may explain why
targeting single pathways is not very effective.

### Malignant cells intra-tumoral heterogeneity dominated by a few recurrent expression programs

They identified expression programs that varied between cells and then found the
recurrent ones or meta-modules. 44% of signatures were associated with cell
cycling. The remaining expression signatures were consistent across their tumor
samples which suggests that despite differences between tumors they share
fundamental processes that are reflected in their heterogeneity patterns. These
signatures formed four main groups with 39-50 genes in each and recurred across
the overlapping signatures from multiple tumors.

Two meta-modules were associated with mesenchymal-related genes that were
defined as mesenchymal-like. The other four were associated with neural
development characteristic of progenitor cells like OPCs and NPCs. These
meta-modules mimic developmental cell types with distortions from normal
expression programs.

### Cycling cells and hybrid cellular states

They classified the tumor cells by meta-module expression and cell cycle
programs. Cycling cells were between 3 and 51% and enriched in OPC-like and
NPC-like states. 15% of the states expressed two modules and were defined as
being in a hybrid state. This data suggests a model where tumor cells span four
main cellular states and each state has proliferative potential, with NPC and
OPC-like states with the highest proliferative potential.

### Limited relationship between genetic subclones and intra-tumoral state diversity

To see whether intra-tumoral cell state diversity reflects genetic subclones,
they examined the subclones and the cell states that fell within them. All the
clones had the four states in them showing that the clonal category did not
reflect cellular state. The differentially expressed genes between the subclones
were not associated with the meta-modules.

### Defined genetic drivers influence the distribution of cellular states

The frequencies of states varied between the tumors and sometime even between
regions in a tumor, but the tumors had at least two states in them. There tended
to be one or a combination of two states that was dominant in the tumors and
that corresponded to the subtypes found earlier. The classical type had
astrocyte-like enrichment while the mesenchymal-like had mesenchymal-like cell
type enrichment. The proneural subtype corresponded to a combination of the OPC
and NPC-like types. OPC-like and NPC-like tend to co-occur in glioblastoma and
are difficult to distinguish in bulk RNA-seq.

They hypothesized that genetics and the tumor micro-environment are responsible
for the fact that each tumor contains multiple cell types while also having one
or two enriched types. This environment may be favoring or inhibiting
transitions between states. They looked for differentially expressed genes
between the states that are not part of that state's expression program. For
tumors with enriched AC-like cells, they found an upregulation of _EGFR_
compared to tumors without AC-like cell type environment. _EGFR_ acts as a
regulator of astrocytic differentiation. Similarly _PDGFRA_ was associated with
the enrichment of the OPC-like cell type and _CDK4_ with the enrichment of the
NPC-like cell-type; the OPC-like and APC-like had differential associations
despite being found together in the proneural subtype.

Using bulk data they scored each sample for expression of the meta-module genes
and from the associations between expression scores and genetic features, they
saw that _EGFR_, _PDGFRA_, and _CDK4_ amplifications were associated with higher
AC-like, OPC-like, and NPC-like scores respectively. Point mutations in _NF1_
were correlated with the enrichment of the mesenchymal-like cell type, but
chromosomal aberrations had stronger effects on cell state enrichment.

### _EGFR_ drives an AC-like program and _CDK4_ an NPC-like program in mouse neural cells

Next they proposed that the genetic drivers they found may favor specific cell
states by inducing growth or favoring transitions. They overexpressed the
regulatory genes in mouse neural progenitor cells and did scRNA-seq. NPCs
overexpressing _EGFR_ induced an AC-like program and those overexpressing
_CDK4_ induced an NPC-like program. These oncogenes favor the transition of
non-cancer progenitor cells to states that they correlated with in tumors. Both
_EGFR_ and _CDK4_ are proliferative drivers and the mouse neural progenitor
cells proliferated more with _CDK4_ than with _EGFR_ while in mouse astrocytes,
_EGFR_ had a stronger proliferative effect. Cell types may respond to different
oncogenes.

### Demonstration of cellular plasticity by combined scRNA-seq and cellular barcoding

Genetics can drive the identity of cellular states, but the skew is incomplete
resulting in a heterogeneity of states maintained through  cellular plasticity.
They tested cell ability to transition between states using xenografts and
checking the state distribution in the tumor.

They isolated cell types by finding cell-surface markers from the meta-module
genes and selected a tumor with a _EGFRvIII_ alteration with a high AC-like
proportion. After injection into the mice, they developed glioblastomas. At
first they had different proportions of cell types, but over time they matched
the proportions of the initial tumor sample, recapitulating the baseline
distribution of states in mice.

They then showed plasticity by modifying a glioblastoma mouse model with H-Ras
and shP53 lentiviruses. scRNA-seq of the tumors formed showed that they had
three of the four cell types in them and that the barcodes added were found
among cells in different states. With proliferation, heritable barcodes added to
them were found in cells in different states showing common plasticity among
states.

With human patient cell cultures and a similar procedure, they found the same
barcode in different states showing that a single cell can lead to four
glioblastoma states.

