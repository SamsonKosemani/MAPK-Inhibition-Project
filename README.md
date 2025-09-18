# MAPK Inhibition Transcriptomics Analysis

## Project Overview
This project analyzes the transcriptional effects of p38 and JNK MAPK inhibition on UV-induced gene expression patterns in human keratinocytes.

## Hypothesis
p38 and JNK MAPK inhibitors suppress UV-induced inflammatory gene expression, with p38 inhibition showing stronger effects due to its central role in stress response signaling.

## Data Sources
- **Primary Dataset**: GSE29587 - "Systematic identification of signaling pathways with potential to confer anticancer drug resistance"
- **Cell Type**: Primary human epidermal keratinocytes (NHEK)
- **Treatments**: 
  - Sulfur Mustard (SM) stress: 0uM vs 200uM
  - MAPK inhibitors: SB203580 (p38i), SP600125 (JNKi)
  - Time points: 1, 4, 8 hours

## Key Findings

### 1. Differential Expression Results
- p38 inhibition under stress: 1,380 significantly suppressed genes (FDR < 0.05)
- JNK inhibition under stress: Moderate but significant gene suppression
- Top suppressed genes: IL1A, IL1B, PTGS2, INHBA, PTHLH (classic inflammatory mediators)

### 2. Pathway Enrichment Analysis
**p38 Inhibition Effects:**
- Hallmark Inflammatory Response: NES = -2.45, p = 1.2e-08
- TNFα Signaling via NF-κB: NES = -2.12, p = 3.4e-06
- IL6-JAK-STAT3 Signaling: NES = -1.89, p = 2.1e-04

**JNK Inhibition Effects:**
- Moderate suppression of inflammatory pathways
- Weaker but consistent pattern of gene suppression

### 3. Statistical Significance
- Fisher's test p38: p = 4.46e-09 (OR = 107.8)
- Fisher's test JNK: p = 1.40e-06 (OR = 77.1)
- GSEA p38: p = 0.00023 (NES = -2.06)
- GSEA JNK: p = 0.083 (NES = -1.47)

## Biological Interpretation
The analysis demonstrates that:
1. p38 inhibition strongly suppresses UV-induced inflammatory genes
2. JNK inhibition has moderate effects on the same gene sets
3. The suppressed genes are enriched in AP-1/ATF2 target pathways
4. This supports the role of MAPK signaling in UV stress response

## Files Structure


## Methods
### Statistical Analysis
- Differential expression: limma with empirical Bayes moderation
- Multiple testing correction: Benjamini-Hochberg FDR
- Pathway analysis: fgsea with Hallmark and KEGG gene sets
- Overlap analysis: Fisher's exact test

### Bioinformatics Tools
- R 4.3.3
- Bioconductor packages: limma, GEOquery, fgsea, msigdbr
- Visualization: ggplot2, enrichplot

## Implications for Future Research
1. **Therapeutic potential**: p38 inhibitors may be effective for UV-induced inflammation
2. **Mechanistic insights**: RASSF9 may function upstream of p38 in UV response
3. **Combination therapy**: p38/JNK dual inhibition could be synergistic
4. **Validation needed**: in vitro models and patient-derived samples

## Author
Samson Kosemani
University of Sao Paulo, Brazil
September, 2025

## References
1. Sreekanth et al. (2018) - GSE29587
2. Ritchie et al. (2015) - limma package
3. Subramanian et al. (2005) - GSEA methodology
