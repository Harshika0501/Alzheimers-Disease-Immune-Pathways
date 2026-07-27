# AD Risk Genes: Immune Pathway Involvement

## Overview
This project investigates the extent to which established Alzheimer's disease (AD) risk genes are involved in immune system-related biological processes, using publicly available pathway and protein interaction databases.

## Data source
The gene list (n = 76 unique genes) was compiled from Tables 1 and 2 of:

> Bellenguez, C. et al. (2022). New insights into the genetic etiology of Alzheimer's 
> disease and related dementias. *Nature Genetics*, 54, 412–436. 
> https://doi.org/10.1038/s41588-022-01024-z

This study identified 75 genome-wide significant risk loci for AD and related dementias (33 previously known, 42 new at the time of publication) from a two-stage GWAS meta-analysis of 111,326 clinically diagnosed/proxy AD cases and 677,663 controls.


## Results

- **76** AD risk genes were compiled from the source GWAS.
- Unbiased enrichment across the full gene list recovered both amyloid-processing terms (e.g., regulation of amyloid-beta formation/clearance) and immune terms (e.g., immune effector process, myeloid leukocyte activation) among the top 10 most significant Biological Process terms- independently reproducing the two  major biological themes reported by Bellenguez et al. without pre-selecting for either.
- **26 of 76 genes (34%)** were identified as immune-relevant across GO, KEGG, and Reactome enrichment, cross-validated against STRING's independent enrichment output and confirmed by manual functional review.
- STRING network analysis showed immune-flagged genes (including TREM2, SPI1, PLCG2, BLNK, INPP5D, TREML2) forming a distinct, densely interconnected cluster, visually separable from an amyloid-processing gene cluster (APP, SORL1, CLU, APH1B, ABI3, CTSB).
- Of the genes the original paper explicitly discussed as immune/microglia-linked  in its main text (TREM2, RHOH, BLNK, SIGLEC11, LILRB2, SHARPIN, RBCK1, OTULIN, ADAM17, TNIP1, SPPL2A), 9 of 11 were independently recovered by this analysis.

## Tools used
- Python (pandas)
- Enrichr (https://maayanlab.cloud/Enrichr/)
- STRING (https://string-db.org/)
- GWAS Catalog (https://www.ebi.ac.uk/gwas/) — used for exploratory reference only

## Repository structure
- `data/` — gene lists (full 76-gene set, immune-flagged subset)
- `results/` — enrichment tables and network figures
- `AD Immune Enrichment Analysis.md` — full methodological log and reasoning

## Relevance
This project reflects a specific interest in the immune dimension of neurodegenerative disease — the overlap between innate immunity, microglial function, and neurodegeneration.
