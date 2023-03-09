---
categories: ["lineage tracing", "epigenetics", "intro", "clocks"]
date: April 12, 2022
date-modified: Jun 06, 2022
doi: 10.1002/path.5911
---

# Lineage tracing in human tissues {.unnumbered}

> Gabbutt C, Wright NA, Baker AM, Shibata D, Graham TA. Lineage tracing in human
> tissues. J Pathol. 2022 Apr 12. doi: 10.1002/path.5911. Epub ahead of print.
> PMID: [35415852](https://pubmed.ncbi.nlm.nih.gov/35415852/).

Lineage tracing is a tool to detect cellular parent-daughter relationships using
clonal markers. Somatic cells carry a many DNA and epigenetic mutations from the
zygote stage that results in patchwork of genetic makeup and can be used to
delineate lineages. The general mutation rate is low enough that distant cells
tend not to have similar mutations. Cells that share mutation tend to be
related. Lineage tracing is necessary to study the dynamics of adult cell
division and can be used to better understand cancer evolution.

### Germline mutations and clonal mosaicism  

Early studies used X-inactivation to study lineage as the silencing of one
X-chromosome is random and leads to a mosaic body. However the timing of markers
and the rates at which they are introduced affects what we can observe and
infer. X-inactivation studies are biased towards finding monoclonal cancer
origin because the inactivation occurs early in development. Rare genotypes can
also be used to study linage as the phenotype can be traced through these
mutations and the mosaicism from X-inactivation.


### MtDNA mutations

Mitochondrial mutations occur at a higher rate than somatic mutations which
makes them more prevalent in samples, but are slow enough to be unique to cells
and clones making them useful for lineage tracing. In addition to the genetic
data, there are also changes in protein expression that can be used to show
clonal relationships.

In colon tissue from older people, cypts were either **CCO**[cytochrome *C*
oxidase]{.aside} proficient, deficient or a mixture. When a CCO- mutation
occurs, there is a partial CCO- crypt which then clonally expands till the
mutant allele reaches fixation leading to a fully CCO- crypt. This showed that
crypts are maintained by a stem cell pool rather than an asymmetrically dividing
stem cell. 

MtDNA is also a part of ATACseq and scATACseq allowing for sensitive detection
of somatic mtDNA mutations.


### Mathematical analysis of single-label lineage-tracing data

The branching process of clonal expansion can be modelled and the parameters
that govern stem cell evolution inferred from static data. The mathematics can
model the dynamical processes of evolution. They also provide a framework for
experimental design and hypothesis testing and expose assumptions about the
biology.


### Somatic epimutations

Along with genetic data, epigenetic information can also be used to conduct
lineage tracing. The profiles of methylated and unmethylated CpG loci can be
compared by their patterns and the Hamming distance between them. Average
methylation increases with cell divisions and age, making it a biological clock.
Methylation data also shows how tumor cells may epigenetically differ from
normal cell in their lineage markers.

### Lineage tracing with WGS

WGS can be used to track somatic nuclear DNA mutations that uniquely mark cells.
Multiregion WGS shows that normal tissue is more mutationally altered than
expected and there are large clonal patches with cancer driver mutations across
tissue types. WGS data can be used to measure mutation rates and timings, and
advantages of driver mutations. This data can also be used to predict future
evolution.
