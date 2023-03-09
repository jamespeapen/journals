---
categories: ["state-space", "gene regulatory networks"]
date: October 19, 2016
date-modified: August 09, 2022
doi: https://doi.org/10.1371/journal.pcbi.1005146
---

# DREISS: Using State-Space Models to Infer the Dynamics of Gene Expression Driven by External and Internal Regulatory Networks {.unnumbered}

> Wang D, He F, Maslov S, Gerstein M. DREISS: Using State-Space Models to Infer
> the Dynamics of Gene Expression Driven by External and Internal Regulatory
> Networks. PLoS Comput Biol. 2016 Oct 19;12(10):e1005146. doi:
> 10.1371/journal.pcbi.1005146. PMID:
> [27760135](https://pubmed.ncbi.nlm.nih.gov/27760135/); PMCID: PMC5070849.

[PLoS Computational Biology](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005146)

This methods paper uses state-space models to study gene expression patterns and
their regulatory networks. This model system decomposes time-series expression
data into components driven by the external regulatory network and the internal
regulatory network. 

A state-space model is generally of the form 

$$ \dot{X} = AX + BU$$ {#eq-general}

where

- $\dot{X}$ is the differential state vector and $X$ is the state vector,
- $U$ is the input vector,
- $A$ is the system matrix,
- $B$ is the input matrix.

In a biological context given that 

- $\mathfrak{R}$ is the real number domain,
- $\Omega$ is the internal gene set made of $N_{1}$ genes,
- $\Psi$ is the external gene set made of $N_{2}$ genes,
- $X_{t} \in \mathfrak{R}^{N_{1} \times 1}$, 
- $U_{t} \in \mathfrak{R}^{N_{2} \times 1}$, 
- $A \in \mathfrak{R}^{N_{1} \times N_{1}}$: the causal interactions between
  genes in $\Omega$, and
- $B \in \mathfrak{R}^{N_{1} \times N_{2}}$: the causal regulations of genes
  in $\Psi$ on genes in $\Omega$

the state space model is 
$$X_{t+1} = AX_{t} + BU_{t}$$ {#eq-gene-regulation}


Then since $X_t = AX_{t-1} + BU_{t-1}$, and $X_{t-1} = AX_{t-2} + BU_{t-2}$ @eq-gene-regulation becomes

$$X_{t} = \underbrace{A^{t-1}X_{1}}_{X_{t}^{INT}} +
\underbrace{\sum\nolimits_{k=1}^{t-2}A^{k}BU_{t-1-k}}_{X_{t}^{INTER}} +
\underbrace{BU_{t-1}}_{X_{t}^{EXT}}$$ {#eq-gene-regulation-t-1}

where 

- $X_t^{INT}$ is the expression vector of the gene components driven only
  internally by genes in $\Omega$,
- $X_t^{INTER}$ is the expression vector of gene components in $\Omega$ driven
  by interactions between internal and external groups.
- $X_t^{EXT}$ is the expression vector of gene componets driven only by the
  genes in $\Psi$.

This separates the expression data into its internal and external components.
