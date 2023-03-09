---
categories: ["rna velocity", "single-cell", "transcriptomics"]
date: August 26, 2021
date-modified: May 26, 2022
doi: 10.15252/msb.202110282
---

# RNA velocity—current challenges and future perspectives {.unnumbered}

[Molecular Systems Biology](https://www.embopress.org/doi/full/10.15252/msb.202110282)

> Bergen V, Soldatov RA, Kharchenko PV, Theis FJ. RNA velocity-current
> challenges and future perspectives. Mol Syst Biol. 2021 Aug;17(8):e10282. doi:
> 10.15252/msb.202110282. PMID:
> [34435732](https://pubmed.ncbi.nlm.nih.gov/34435732/); PMCID: PMC8388041.

RNA velocity models cellular direction and speed in transcriptome space through
the ratio between spliced and unspliced mRNA and its relation to a model.
Positive velocity is interpreted as upregulation while negative velocity is
interpreted as downregulation. The two main approaches to RNA velocity are the
steady-state model and the dynamical model. The steady-state method uses an
observed steady-state between spliced and unspliced mRNA to fit a linear model
and set the threshold for positive and negative velocities. This assumes that
the steady-state can be observed and that the splicing rates are the same across
all genes. If these assumptions are violated, however, the model is prone to
errors in velocity estimates and cellular state predictions. 

### Current limitations

The dynamical model relaxes the steady-state assumption for a more generalized
model of estimation to capture heterogeneous subpopulation and cell-cycle
dynamics. However, it still maintains a deterministic system of differential
equations and constant kinetic rate parameters. A number of cells have multiple
kinetic rates in the same gene or transcriptional boosts that are not
accurately captured by the model. The model also has trouble with fully mature
cell types, predicting arbitrary directions for them. Systems with complex
kinetics like frequently changing kinetic rates are also not well modelled by
the existing methods.

The statistical power of RNA velocity depends on the curvature of the phase
portrait used to decide up or down-regulation. This curvature can be affected by
the time variable kinetic rates of transcription, splicing and degradation. Some
changes results in curvature reduction which reduces statistical power. Others
result in a curve flip which changes some positive velocities to negative ones
and leads to incorrect interpretations of such velocities as downregulation.

### Extensions and future directions

#### Stochastic model

The current RNA velocity models use simple first-order equations with constant
kinetic rates, despite the fact that only a few genes can be captured with this
simple system. Future extensions need to account for dynamic changes in kinetic
rates to improve velocity predictions, accounting for alternative processes that
modulate transcription, splicing and degradation. Identifying time variable rates will also need constraints like a pseudotime prior. 

#### Multivariate models towards system dynamics

Transcriptional and post-transcriptional regulations affect dynamic changes in
gene expression. The current models treat each gene independently and ignore
regulatory relationships. A multivariate model can describe cell-state
transitions and the regulatory interactions involved in the transitions. We can
see regulatory events in a trajectory as expression changes along pseudotime.
The best model would model both the RNA velocities and the regulatory network
from observed expression and kinetics models. Inclusion of other modalities like
chromatin modifications and RNA polymerase activity can provide significant
support.

#### Multi-modal omics models

In addition to the unspliced and spliced data we can also use other modalities
like protein dynamics. In general modalities that can capture abundance, of
which intronic reads are only noisy approximations, can be used to improve
velocity modelling. For intronic reads, improved preprocessing may be helpful in
reducing noise.

### Technical challenges and extensions

Cell size normalization is currently used, but it can distort size effects.
Changes in global factors like splicing efficiency or RNA polymerase abundance
can affect kinetics and need to be accounted for in the model. Current models do
not deal with batch effects since applying a correction to spliced and unspliced
independently may reduce the information we have between them. Gene selecting
can also affect the predictions since only genes that capture data variability
are kept. 

If whole cell isolation is hard to isolate, single nuclei can be used. However,
they are not necessarily representative and can distort the spliced/unspliced
ratio and assumptions about constant kinetics and nuclear export are not
verified.

