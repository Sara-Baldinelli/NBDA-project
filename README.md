# Network-based Data Analysis of RNA Expression in ALS
Project for the Network-based Data Analysis course held by Professor Mario Lauria at University of Trento (M.Sc. in Quantitative and Computational Biology, 2023-2024).

## Project Overview
This repository contains the report of the study of RNA expression profiles among different survival groups in Amyotrophic Lateral Sclerosis (ALS). The project aims to uncover significant molecular pathways and gene interactions associated with ALS progression, leveraging various computational techniques and machine learning algorithms. \
The repository also contains the PDF of the poster, related to the project, presented at the SIBBM 2024 - Frontiers in Molecular Biology conference.

## Dataset
The dataset used in this study was obtained from the Gene Expression Omnibus (GEO) under accession number [GSE212131](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE212131). It contains transcriptomic data from lymphoblastoid cell lines of 42 ALS patients, split into two groups:
- Short Survival Group: Patients with a disease duration of less than 12 months.
- Long Survival Group: Patients with a disease duration of more than 6 years.

## Key Analyses
1. Exploratory Analysis
- Objective: Understand the distribution of gene expression levels across samples and identify potential outliers.
- Methods: Boxplots and Principal Component Analysis (PCA) were used to visualize data characteristics.
2. Clustering Analysis
- Objective: Identify natural groupings within the dataset using unsupervised learning techniques.
- Methods: K-means and Hierarchical clustering were performed to explore the dataset structure.
3. Supervised Machine Learning
- Objective: Classify ALS patient subgroups based on gene expression profiles.
- Methods: Several machine learning algorithms were tested, including Random Forest, Linear Discriminant Analysis (LDA), LASSO, and Ridge regression. Random Forest was selected as the optimal model with a mean accuracy of 73.5%.
4. Enrichment Analysis
- Objective: Identify biological pathways significantly associated with ALS progression.
- Methods: The gprofiler2 package was used for functional enrichment analysis, revealing the mRNA splicing process as a key pathway involved in ALS.
5. Network Analysis
- Objective: Discover potential gene interactors and enriched pathways via network-based analysis.
- Methods: The pathfindR package was used to expand the gene set through literature-based links and to analyze interactions among the most important genes identified by the Random Forest model.

## Tools and Libraries Used
R: The primary language used for analysis. \
Packages:
- ggplot2: For data visualization.
- plotly: For interactive 2D and 3D PCA plots.
- caret: For training and evaluating machine learning models.
- rScudo: For classification of molecular profiles.
- igraph: For network analysis.
- gprofiler2: For functional enrichment analysis.
- pathfindR: For pathway analysis and network visualization.

## How to Run the Analysis
Clone the repository:
``` bash
git clone https://github.com/Sara-Baldinelli/NBDA-project.git
```
## Install the required R packages:
``` r
install.packages(c("ggplot2", "plotly", "caret", "rScudo", "igraph", "gprofiler2", "pathfindR"))
```
## Results and Discussion
The analysis revealed that the mRNA splicing process, particularly involving heterogeneous nuclear ribonucleoproteins (hnRNPs), plays a significant role in the variability of ALS disease duration. Additional pathways, such as antigen processing and IL-17 signaling, were also implicated in the disease's progression.

## Future Work
Further research is needed to validate these findings through experimental approaches and to integrate other omics data for a more comprehensive understanding of ALS.
