---
categories: []
date: July 29, 2015
date-modified: March 21, 2025
doi: 10.1128/mmbr.00006-15
---

# An Overview of Genome Organization and How We Got There: from FISH to Hi-C

[Microbiology and Molecular Biology Reviews](https://journals.asm.org/doi/10.1128/MMBR.00006-15)

> Fraser J, Williamson I, Bickmore WA, Dostie J. An Overview of Genome
> Organization and How We Got There: from FISH to Hi-C. Microbiol Mol Biol Rev.
> 2015 Sep;79(3):347-72. doi: 10.1128/MMBR.00006-15. PMID:
> [26223848](https://pubmed.ncbi.nlm.nih.gov/26223848); PMCID: PMC4517094.

## Genome Organization

Interactions between chromatin and the nuclear lamina occur through Lamin
Associated Domains (LADs) which can be cell-type specific. Chromatin near the
lamina generally has low GC content and are gene poor. Similarly Nucleolus
Associated Domains also have GC- and gene-poor chromatin regions as does
chromatin localized in the nucleolus.

Within the nucleus the genome is broadly divided into chromatin territories.
Chromosomes fold into territories and individual chromosomes fold into active or
open A compartments and closed or silent B compartments. Within compartments,
chromatin is organized into topologically associated domains (TADs) which may be
generally conserved between cell types and across species. Sub-TADs topology
vary with tissue.

[ ![](https://journals.asm.org/cms/10.1128/mmbr.00006-15/asset/8377dbcb-0fe0-41d2-8334-1e3e448281c0/assets/graphic/zmr0031523970003.jpeg) ]{.aside}

### Chromosome territories (CTs)

Chromosomal interactions tend to be more within than between them. Homologous
chromosomes are far from each other in diploid cells and haplotypes don't
interact frequently. Examining DNA with FISH shows that chromosome form
individual domains. There is a cell-specific 'intermingling' between these CTs,
but how much is unknown.

Gene-rich chromosomes tend to be nearer the nuclear center and small gene-rich
chromosomes like 19 interact more with each other than with other small, but
gene-poor, chromosomes, which are found more at the periphery.

The importance of chromosome position and interactions are not fully understood.
The position of CTs can be cell-type specific but can vary a lot between cells.
Gene regulation in there cells may be controlled by the position of genes as
genes deep in a CT are harder to activate.

### Chromosome compartments

PCA of Hi-C data shows contact frequencies grouping into open A compartment or
closed B compartments. A compartments have higher GC content, more gene
enrichment, transcription activity, DNAse I hypersensitivity and active
(H3K36me3) and poised (H3K27me3) chromatin histone modifications. B compartments
have H3K9 silencing marks. B compartment position is highly correlated with late
replication timing and LADs. The distribution of CTs and compartments along
chromosomes is stable across cell-types, but can vary. However,
within-compartment contacts are weak and they may be a transient feature.


### TADs

TADs are blocks of chromatin that interact more with each other than with nearby
regions. They show up as sharp contact frequency changes between regions in 5C
and Hi-C data. Modifying TAD boundary sequences can cause partial domain fusion
and affect nearby gene expression.

> TADs are thought to partition genomes into distinct globular units that can
> remain spatially distant even if they are adjacent along chromosomes. Most
> long-range gene regulation by enhancers is constrained within TADs.

### Sub-TADs


TADs can be divided into Sub-TADs. Large TADs found previously could be divided
into smaller domains that were stable between cell lines and whose boundaries
had enriched CTCF binding and activating histone marks. At this level, chromatin
organization is tissue-specific.

### Looping


Chromatin can have long range interactions through looping which promotes or
prevents contact between promoters and regulatory elements like enhancers.
> cellular enhancers have been found genome-wide and are largely responsible for
> the tissue-specific expression of genes enhancers can activate transcription
> in either orientation, whereas promoters cannot. Enhancers can also drive
> transcription from a position upstream of, downstream of, or within target
> genes.

> Long-range promoter interactions were often not blocked by CTCF and cohesin
> binding sites and that enhancers physically interact with the nearest gene in
> only 7% of cases. Interactions between promoters and sequences were most
> frequent 120 kb upstream of transcription start sites and were asymmetric,
> suggesting a directionality of chromatin looping.


:::{.aside}
Cell-type specific elements

- LADs: those with high GC content and correlate with tissue-specific gene
  expression

- TADs

- The position of CTs and compartments along the chromosome
:::


## Key regulators of genome architecture

### CTCF and gene regulation

CTCF is a highly conserved protein that can bind to DNA insulator sequences
which suppress transcription. It can bind to more than 30,000 sites and
frequently bound sites have genes with tissue-specific promoters. It may also be
involved in LAD formation. CTCF can form long-range DNA contacts and spatially
organize chromatin as part of its insulator function.

### Cohesin

Cohesin is a protein complex involved in sister chromatid cohesis, chromosome
segregation and DNA repair as well as transcription regulation.
> Cohesin colocalizes extensively with CTCF throughout the genome. In fact, many
> of the original CTCF-mediated looping contacts were later found to require
> cohesin.

> By physically segregating chromatin regions into topological domains, CTCF and
> cohesin might define functional microenvironments for regulatory elements and
> target genes where contacts are more easily nucleated while preventing
> chromatin states from spreading and limiting contacts with the rest of the
> genome. The partitioning of the genome into TADs correlates with
> enhancer-promoter units, clusters of coregulated promoters and enhancers.
> Cohesin may organize chromatin in such a way as to prevent interactions
> between particular TADs and isolate gene expression states from one another

## Assays



### Chromatin conformation capture (3C)

3C can examine genomic organization in short regions as high resolution as
interactions are measured individually. 3C cannot easily distinguish between
haplotypes and reads are averaged between chromosomes, along with any
abnormalities. Data are averaged chromatin interaction patterns and does not
have interaction stability or strength information or cell-specific information.
Variability from cell cycle stage can affect chromatin conformation.

### Chromatin conformation capture-on-chip (4C)

4C improves on the throughput and resolution of 3C with microarrays and
sequencing. However, it only captures interactions between one restriction
fragment and the rest of the genome and its data cannot be used to predict
domain or chromosome-level conformation.

### Chromosome conformation capture carbon copy (5C)

5C can detect up to millions of 3C ligation junctions between many restriction
fragment pairs simultaneously, as long as the regions are covered by the primer
library.


### HI-C

Hi-C is also called genome-wide chromosome conformation capture and can study
the spatial organization of an entire genome. Hi-C complexity is very high and
the deep sequencing required is expensive. 4C and 5C are better for
submegabase-scale analyses.
