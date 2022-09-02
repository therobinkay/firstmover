# Influence of the first-mover advantage on the gender disparities in physics citations (2022)

## Description
This repository contains the code and data to produce tables and figures for *Influence of the first-mover advantage on the gender disparities in physics citations* by Hyunsik Kong, Samuel Martin-Gutierrez, and Fariba Karimi: https://arxiv.org/abs/2110.02815

### Abstract
Mounting evidence suggests that STEM fields (Science, Technology, Engineering, and Mathematics) suffer from gender biases. In this paper, we study the physics community, a discipline where women are still under-represented and gender disparities persist. To reveal such inequalities, we perform a paper matching analysis using a robust statistical similarity metric. Our analyses indicate that women’s papers tend to have lower visibility in the citation network, a phenomenon significantly influenced by the temporal aspects of scientific production. Within pairs of similar papers, the author that publishes first tends to obtain more citations. By controlling for publication date, the gender disparity among first and last authors decreases by 31% and 15%, respectively. From the group perspective, men have cumulative historical advantages due to women joining the field later and at a slower rate. Therefore, the first-mover advantage plays a crucial role in the emergence of gender disparities in the physics community.

## Folder Structure

### Data
- result.csv
- paperdata.csv
- primdata.csv
- lastdata.csv
- citationBara.csv
- mfpairs_similarity.csv
- mwpairs_similarity_edited.csv
- mmpairs_similarity.csv

### Codes

#### data_preprocess.ipynb
...

#### Creating_pairs.ipynb
...

#### stat.ipynb
- Basic journal statistics, author participation statistics
- Author order analysis
- Career age / productivity analysis (K-S test)
- Dropout analysis

#### network.ipynb
- Self-citation analysis / statistics
- Degree / PageRank centrality statistics (Women author proportion)
- Centrality vs. productivity visualization

#### similarity.ipynb
- Similarity validation statistics
- Centrality difference trend
- Comparison analysis of m-m pairs and m-w pairs
- Subfield visualization, Wilcoxon tests

#### additional_visualization.ipynb
- Quadrant / heatmap visualization (Figure 3B, 3C)
