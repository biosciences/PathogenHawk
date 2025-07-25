---
title: 'PathogenHawk: A Pathogen Machine Learning Toolkit for Predicting Antimicrobial Resistance from Genomic Features'
tags:
  - bioinformatics
  - antimicrobial resistance
  - machine learning
  - fungal genomics
  - pathogen genomics
  - Python
  - XGBoost
authors:
  - name: Kaitao Lai
    orcid: 0000-0000-0000-0000
    affiliation: 1
affiliations:
  - name: The University of Sydney
    index: 1
date: 2025-07-20
bibliography: paper.bib
---

# Summary

**PathogenHawk** is an open-source machine learning toolkit for predicting antimicrobial resistance (AMR) across fungal and bacterial pathogens using whole genome sequencing data. It is designed to support research in translational bioinformatics, clinical microbiology, and genomic epidemiology. PathogenHawk provides an end-to-end pipeline from variant calling to feature extraction, model training, and interpretation.

We demonstrate the utility of PathogenHawk with *Candida auris*, an emerging fungal pathogen with multidrug resistance, using public genomic annotations and simulated resistance profiles. The toolkit enables reproducible model development with interpretable output and can be extended to other species such as *Escherichia coli*, *Staphylococcus aureus*, and *Aspergillus fumigatus*.

Key features include:
- Integration of variant- and gene-based features
- Configurable ML pipelines with support for XGBoost [@xgboost2016]
- Visualization of feature importances and confusion matrices
- Compatibility with Nextflow for scalable workflows

# Statement of need

Despite the growing availability of microbial whole-genome data, there is a lack of lightweight, interpretable, and extensible tools for AMR prediction that work across different pathogens. PathogenHawk addresses this gap by offering a cross-species framework for AMR prediction based on machine learning [@syntchenko2024ai], designed for bioinformaticians, microbiologists, and computational epidemiologists.

# Implementation

PathogenHawk is implemented in Python and optionally uses Nextflow for scalable preprocessing workflows. Key dependencies include `xgboost`, `scikit-learn`, `pandas`, `matplotlib`, and `PyYAML`.

The toolkit includes:
- YAML-driven configuration
- Precomputed or VCF-based feature support
- Training and evaluation scripts
- Jupyter notebooks for demonstration
- Synthetic and real data integration

# Example

An example use case using *Candida auris* is provided in `demo_cauris.ipynb`, with synthetic mutation profiles and resistance labels derived from MIC thresholds. Feature importance rankings and confusion matrices are automatically visualized after model training [@candidaauris2019].

# Acknowledgements

We acknowledge the contributions of public datasets from NCBI and annotation resources from NCBI RefSeq and Ensembl Fungi. We also thank Prof. Vitali Sintchenko for his inspiration through his recent work on AI applications in pathogen genomics [@syntchenko2024ai].

# References

::: {.bibliography}
:::
