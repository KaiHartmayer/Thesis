# Structured Insights from Unstructured Text Data
## Machine Learning-Based Patent Analysis to Determine the Position of New Technologies Within the Innovation Cycle

[![Python](https://img.shields.io/badge/Python-3.10.13-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## Overview

This repository contains all code and data necessary to replicate the analysis presented in our paper on using machine learning to analyze patent texts and determine technology positions within innovation cycles, with lithium-ion batteries as a case study.

---

## Repository Structure

### Core Analysis Files

| File | Description |
|------|-------------|
| `df_lemma_dropped.ipynb` | **Data preprocessing pipeline** - Cleans and prepares patent text data, saves working dataframe as CSV |
| `descriptives.ipynb` | **Descriptive statistics** - Generates all descriptive statistics reported in the Results section |
| `time_period_analysis_plots.ipynb` | **Temporal visualizations** - Creates plots of structured data over time (first plot appears in paper) |
| `demonstration_simplified.ipynb` | **Method demonstration** - Reproduces the simplified example figure from the Methods section |
| `max_tree_depth_check.ipynb` | **Robustness check** - Tests result stability across different maximum tree depths (3, 5, and 7) |

### Main Analysis Pipeline
> **Note:** Due to RAM limitations, the main analysis has been split across multiple notebooks

| File | Description |
|------|-------------|
| `get_tfidf_dummy.ipynb` | **Feature engineering** - Creates word pair variables, applies filters, exports to CSV |
| `1920-2016_BorutaShap_HDBSCAN_UMAP_viz.ipynb` | **Feature selection & clustering (1920-2016)** - Runs Boruta-SHAP algorithm with UMAP-HDBSCAN visualization |
| `2017-2023_BorutaShap.ipynb` | **Feature selection (2017-2023)** - Runs Boruta-SHAP for most recent time period |
| `get-accepted-sentences-qualitative-analysis.ipynb` | **Qualitative extraction** - Extracts sentences containing important word pairs, exports to XLSX; plots average feature importances |
| `QualEval.ipynb` | **Validation analysis** - Calculates inter-rater reliability (Cohen's κ) and analyzes response frequencies |

---

## Data Files

### Patent Dataset
- **`df_lemma_dropped_part1.zip`** and **`df_lemma_dropped_part2.zip`** 
  - Combined, these files contain the complete preprocessed patent dataset (n=57,052) used in the case study
  - Extract both parts to reconstruct the full dataframe

### Qualitative Evaluation
- **`Qualitative_Part/`** folder
  - Contains responses to all 6 evaluation questions for sampled patents
  - All patents rated on the 3 sufficiently reliable questions by Rater 1 (primary author)
  - Includes domain expert ratings for validation

---

## Getting Started

### Prerequisites
```bash
Python 3.10.13
