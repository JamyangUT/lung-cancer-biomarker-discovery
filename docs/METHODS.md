# Documented Methods

These methods summarize the 2025 group report and accompanying manuscript. They describe the original work; no analysis has been rerun for this repository.

## Study design

The project compared publicly deposited lung tumor and non-tumor tissue expression profiles. The report describes a retrospective, computational biomarker-discovery study without wet-lab validation.

Ten GEO accessions are named in the documents, while multiple methods and results passages describe analysis of eight datasets. The exact eight-dataset subset cannot be established from the available documents. The [data page](DATA.md) therefore labels all ten as referenced accessions rather than confirmed analysis cohorts.

## Differential expression and enrichment

- Dataset-specific differential expression used GEO2R and R/limma.
- The results sections specify a filter of **p < 0.05 and |logFC| > 1**. Some methods passages write the fold-change condition differently; the original scripts would be needed to resolve the implemented expression.
- DEG result tables were concatenated in R, and gene-symbol intersections were used to identify common candidates.
- Gene Ontology and KEGG enrichment investigated biological processes and pathways associated with selected genes.

The reports discuss adjusted p-values, but the stated selection filter uses p-values. This repository does not relabel that filter as an FDR-controlled discovery threshold. Concatenating DEG tables also does not by itself establish a statistical meta-analysis or a count of unique genes.

## Network analysis

The common-gene list was submitted to STRING 12.0. Network edges were filtered around a combined-score threshold of 0.4, then imported into Cytoscape 3.10.3. MCODE 2.0.3 identified dense clusters; the highest-scoring cluster was selected for downstream investigation.

The documents describe six clusters and a maximum MCODE score of 15.0. They describe a 16-node selected cluster, while the group report's hub-gene table lists 15 symbols. The exact cluster membership requires the original network export.

## Expression mapping and machine learning

The documents describe mapping selected genes to probe/expression identifiers and creating a matrix with **107 samples and 29 expression features**, with tumor/normal labels. The provenance of the final sample list and harmonization of expression platforms are not fully documented.

In Python, the project used LASSO with cross-validation for the regularization parameter and Random Forest feature ranking. In R 4.4.2, the report describes LASSO, Random Forest, SVM, and Decision Tree models. The reported training/test split was **80:20**.

The original code is needed to establish whether preprocessing, feature selection, and tuning were confined to the training data. No claim of leakage-free or externally validated performance is made here.

## Reproducibility

The original R/Python code, dependency lockfiles, random seeds, sample annotations, expression matrices, fitted models, and network exports are unavailable. Historical tool versions above are reported versions, rather than a tested installable environment.

Reconstruction would require recovering the exact selected accessions, platform-specific preprocessing, sample inclusion rules, gene/probe mapping, contrast definitions, and model evaluation procedure. Any future reconstruction should be labeled as a new analysis and evaluated on independent data.
