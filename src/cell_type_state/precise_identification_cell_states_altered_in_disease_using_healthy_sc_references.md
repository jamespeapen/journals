---
categories: ["cell-state identification", "transcriptomics", "scRNA-seq", "cell
atlas"]
date: October 12, 2023
date-modified: March 13, 2024
doi: 10.1038/s41588-023-01523-7
---

# Precise identification of cell states altered in disease using healthy single-cell references {.unnumbered}

[Nature Genetics](https://www.nature.com/articles/s41588-023-01523-7)

> Dann E, Cujba AM, Oliver AJ, Meyer KB, Teichmann SA, Marioni JC. Precise
> identification of cell states altered in disease using healthy single-cell
> references. Nat Genet. 2023 Nov;55(11):1998-2008. doi:
> 10.1038/s41588-023-01523-7. Epub 2023 Oct 12. PMID:
> [37828140](https://pubmed.ncbi.nlm.nih.gov/37828140); PMCID: PMC10632138.

Although cell atlases exist that can be used to find diseased cell states in a
scRNA-seq dataset, identifying diseased states is best done when there are
matched control samples available to compare against. The atlas may not
correctly reflect the space of the dataset since the atlas data characteristics
would be different to the dataset's. However, only using a matched control is
not always possible and tends to be a small number of cells, making it more
likely that rare cell states are missed or noise is interpreted as signal.

This study tests whether both atlas and control data can be used together to
better identity cell states within a disease dataset. They found that using an
atlas dataset as a reference for latent embedding and a control dataset for
differential analysis can provide benefits from both the atlas and the control.
This process involves training a dimensionality reduction model to capture
relevant cellular phenotypes while also minimizing batch effects. Then, using
transfer learning, the query or control-disease combined dataset is mapped to
that latent space. Differential analysis is done after this mapping to find
differences in gene expression signatures and cell composition.

Although atlas datasets cannot replace real matched controls, they can improve
diseased state detecting and reduce the required number of control samples
without significantly affecting sensitivity. A leave-one-out analysis showed
that the size and composition of the atlas dataset did not negatively impact
diseased state detection. Testing the joint method on real data revealed that it
was more sensitively able to detect "transitional and heterogeneous pathological
cell states".
