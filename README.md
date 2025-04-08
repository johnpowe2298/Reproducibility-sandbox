# README

# Acute Myeloid Leukemia Heatmap Analysis

Analysis of RNA-seq data from acute myeloid leukemia samples using clustering heatmap visualization.

## Overview

This analysis examines gene expression patterns across 19 acute myeloid leukemia (AML) samples from mice under controlled treatment conditions. The dataset originates from [Shih et al., 2017](https://pubmed.ncbi.nlm.nih.gov/28193779/) and has been processed and quantile normalized through [refine.bio](https://www.refine.bio/).

## Dataset Information

* Source: [SRP070849](https://www.refine.bio/experiments/SRP070849)
* Samples: 19 AML model mice samples
* Processing: Quantile normalized RNA-seq data
* Treatment Groups:
  * IDH2 mutant AML (vehicle or AG-221 treated)
  * TET2 mutant AML (vehicle or 5-Azacytidine treated)

## Analysis Pipeline

The analysis follows these key steps:

1. Data Organization
   * Directory structure setup
   * Sample metadata processing
   
2. Gene Selection
   * Variance calculation
   * Selection of top quartile genes
   
3. Visualization
   * Clustering heatmap generation
   * Sample annotation
   * Color gradient visualization

## Required Packages

* [pheatmap](https://www.rdocumentation.org/packages/pheatmap)
* magrittr
* readr
* dplyr
* tibble
* sessionInfo

## Directory Structure

```markdown
project_root/
├── data/
│   └── SRP070849/
│       ├── SRP070849.tsv      # Gene expression matrix
│       └── metadata_SRP070849.tsv  # Sample metadata
├── plots/
│   └── aml_heatmap.png        # Generated heatmap
└── results/
    └── top_90_var_genes.tsv   # Selected high-variance genes
```

## Usage Instructions

1. Clone the repository
2. Create the required directory structure
3. Download the dataset from refine.bio
4. Run the analysis pipeline
5. Generate heatmap visualization

## Output Files

* `aml_heatmap.png`: Clustering heatmap showing expression patterns
* `top_90_var_genes.tsv`: Selected high-variance genes
* Session information report

## Dependencies

The analysis requires R with the specified packages installed. The code is designed to be reproducible with a fixed random seed (12345) for consistent clustering results.

## Citation Information

This analysis was adapted from the [refine.bio-examples notebook](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html) and utilizes data from Shih et al., 2017.