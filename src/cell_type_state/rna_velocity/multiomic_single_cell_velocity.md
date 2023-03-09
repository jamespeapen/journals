---
categories: ["rna velocity", "cell-type vs cell-state", "single-cell", "transcriptomics", "epigenetics", "chromatin remodelling"]
date: Oct 13, 2022
date-modified: Oct 17, 2022
doi: 10.1038/s41587-022-01476-y
---

# Multi-omic single-cell velocity models epigenome–transcriptome interactions and improves cell fate prediction {.unnumbered}

> Li C, Virgilio MC, Collins KL, Welch JD. Multi-omic single-cell velocity
> models epigenome-transcriptome interactions and improves cell fate prediction.
> Nat Biotechnol. 2022 Oct 13. doi: 10.1038/s41587-022-01476-y. Epub ahead of
> print. PMID: [36229609](https://pubmed.ncbi.nlm.nih.gov/36229609/).

[Nature](https://doi.org/10.1038/s41587-022-01476-y)

This paper extends the work of RNA velocity to include chromatin accessibility
in the model. Where the original RNA velocity model had ODEs modelling the
change in spliced mRNA, this model includes the change in chromatin accessibility
as a third equation. This adds a third-dimension to the RNA velocity plots and
gives greater confidence in predicting velocity vectors. In situations where
both spliced and unspliced RNA are not present, it is difficult to predict
direction. With chromatin accessibility, the model can tell whether
transcription is starting or ending by whether chromatin is getting more or less
accessible. Chromatin accessibility rises before gene expression changes and
allows predicting directions that could not be done with gene expression data
alone.

They describe four states that relate the epigenome and transcriptome. The first
primed state is is the period where chromatin accessibility is increasing
without any changes to transcription. Then transcription and chromatin
accessibility increase together until chromatin accessibility starts decreasing.
This is followed by lowered transcription align with continued reduction in
accessibility. The points where chromatin accessibility and transcription move
in the same direction are called coupled stages. When they move in opposite
directions, they are considered decoupled.
