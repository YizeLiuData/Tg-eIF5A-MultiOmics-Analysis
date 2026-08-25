# Toxoplasma eIF5A K49 Ribo-seq analysis scripts

This repository provides the analysis and visualization scripts associated with the manuscript:

**eIF5A K49 acetylation controls the tachyzoite–bradyzoite transition of the zoonotic parasite *Toxoplasma gondii***

## Authors

Yize Liu, Si Zuo, Ning Jiang, Han Yu, Xiaoyu Sang, Ying Feng, Ran Chen, and Qijun Chen

## Analyses included

### Codon-occupancy analysis

The `01_codon64` workflow normalizes P-site counts across the 64 codons and compares codon occupancy between stressed and unstressed parasites. It includes codon-specific tests, effect-size estimation, global correlation analysis, codon ranking, rank heatmaps, volcano plots and Bland–Altman analysis. Dedicated plotting scripts generate publication-ready visualizations of the codon-occupancy results.

### Translation-state score

The `02_state_score` workflow derives a WT-referenced translation-state score from codon-occupancy profiles. It prepares the score inputs, performs the statistical evaluation, generates the corresponding visualization and validates the reproduced outputs.

### Adaptive translational pausing analysis

The `03_apr_pi_rpi` workflow builds the transcript reference, aligns Ribo-seq reads, assigns P-sites and calculates P-site quality metrics. It then computes the pausing index and relative pausing index, evaluates replicate-supported pausing with edgeR, integrates the statistical evidence and identifies finite-positive adaptive translational pausing gene sets. Additional scripts generate metagene, quality-control and pausing visualizations.

### Pausing-set overlap analysis

The `04_apr_overlap` workflow compares finite-positive adaptive translational pausing gene sets between experimental conditions and generates an area-proportional Venn diagram.

### Pre-ranked gene set enrichment analysis

The `05_strict_gsea` workflow performs pre-ranked gene set enrichment analysis by projecting adaptive translational pausing gene sets onto ranked mRNA-seq differential-expression results. It calculates enrichment scores, normalized enrichment scores, nominal and adjusted significance values, and leading-edge subsets, and generates the associated tables and visualizations.

## Repository contents

| Path | Content |
|---|---|
| `01_codon64` | Codon-occupancy analysis and visualization scripts |
| `02_state_score` | Translation-state score derivation, plotting and validation scripts |
| `03_apr_pi_rpi` | Ribo-seq reference construction, alignment, P-site processing, pausing analysis and visualization scripts |
| `04_apr_overlap` | Adaptive translational pausing overlap analysis and Venn-diagram script |
| `05_strict_gsea` | Pre-ranked gene set enrichment analysis, workbook generation and packaging scripts |




## Data availability

Raw sequencing data and large source-data files should be obtained from the accession records associated with the article or from the corresponding public data repository once released.

