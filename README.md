# Tissue-Specific Immune Specialization in the Spleen and Liver

**Author**: Sierra Dahiyat  
**Course**: Bioengineering C149 (Computational Functional Genomics)    
**Date**: December 19, 2024  

---

## Overview

This project investigates the distinct immune roles of spleen and liver cells using **single-cell RNA-seq** data from the **Tabula Muris** dataset. The analysis focuses on transcriptomic differences between tissues, highlighting immune cell specialization using dimensionality reduction, marker gene expression, and cell type annotation.

Key objectives:
- Visualize tissue-specific cell clusters using UMAP and PCA
- Identify marker gene expression patterns (H2-Ab1, Coro1a)
- Explore the distribution of annotated cell types across spleen and liver

---

## Files

| File                  | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| `final_project.ipynb` | Full analysis pipeline including preprocessing, dimensionality reduction, gene expression analysis, and cell type annotation |
| `bioE_final_write_up.pdf` | Final written report summarizing methodology, key figures, results, and discussion |
| **Tabula Muris Data** (not included) | Single-cell RNA-seq count matrices for spleen and liver from the Tabula Muris project |

---

## Dataset

Data was sourced from the **Tabula Muris** Consortium, which includes single-cell RNA-seq profiles from 20 mouse organs. For this project:
- **Spleen matrix**: 1718 cells × 23,434 genes
- **Liver matrix**: 981 cells × 23,434 genes

Data preprocessing steps:
- Removal of genes with zero expression across all cells
- Log-transformation
- Filtering to retain the middle 95% of values

---

## Key Analysis Steps

- Dimensionality reduction using **UMAP** and **PCA**
- Visualization of tissue-specific clusters
- Differential expression analysis of:
  - `H2-Ab1`: MHC class II gene enriched in spleen
  - `Coro1a`: T-cell and actin-regulating gene with tissue-specific expression patterns
- Integration of cell type annotations from the Tabula Muris dataset

---

## Key Findings

- Spleen and liver cells form distinct transcriptomic clusters
- `H2-Ab1` is strongly expressed in spleen B cells, consistent with its immune role
- `Coro1a` shows broad spleen expression but more restricted expression in the liver
- Annotated UMAP plots show clear separation between immune (B cells, T cells, NK cells) and metabolic (hepatocytes, endothelial) cell types

---

## Limitations

- UMAP clusters are unsupervised and may not perfectly reflect biological subtypes
- Only two marker genes were explored in-depth
- No correction for intra-tissue cell type variation during differential expression

---

## References

- Tabula Muris Consortium et al. "Single-cell transcriptomics of 20 mouse organs creates a Tabula Muris." *Nature*, 2018.
- National Center for Biotechnology Information (NCBI). Gene entries for H2-Ab1 and Coro1a.
