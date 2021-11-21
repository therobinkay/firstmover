# First-mover advantage explains gender disparities in physics citations (2021)

## Description
This repository contains the raw and preprocessed datasets and the Python codes run by Jupyter Notebook for *First-mover advantage explains gender disparities in physics citations* by Hyunsik Kong, Samuel Martin-Gutierrez, and Fariba Karimi: https://arxiv.org/abs/2110.02815

## Data & Codes

### Data
#### cdata.csv
A processed dataset that shows **data.csv** data columns for both citing and cited papers from **citationBara.csv**.
#### cen.csv
A processed dataset that shows the DOI and primary author gender of both citing and cited papers from **citationBara.csv**.
#### citationBara.csv
A raw dataset that shows a mass citation network relationship. Consists of the following data columns:
- *citing_doi*: DOI of an article that cites
- *cited_doi*: DOI of an article that is cited
#### data.csv
A processed, fundamental dataset for most analyses. Consists of the following data columns:
- *doi*: Digital object identifier (DOI) of each article
- *id*: Author id
- *gender*: Author gender
- *order*: The listed position of author in the particular publication
- *numAuthor*: Number of participating authors
- *is_last*: True if the author is the last author of the publication
- *is_alpha*: True if this article lists authors alphabetically
- *year*: Publication year
- *articleType*: Type of article
- *journal*: The journal the publication is published in
#### doipacs.csv
A raw dataset that shows the DOI and the subfield of each article. Processed into other datasets and is therefore not used.
#### pairdata.csv
A processed dataset that shows all paired atricles. A concatenated dataset of all data in **sims.zip**.
#### sim0 - sim9
A processed dataset that shows paired articles. Consists of datasets for all 10 subfields, with the following data columns:
- *paper*: Digital object identifier (DOI)
- *gender*: Gender of its primary author
- *year*: Publication year
- *qval*: q-value, mentioned in the similarity algorithm
- *k*: k-measurement for missing link analysis; not used for this article
#### sim_mm.csv
A processed dataset that shows paired male articles. Consists of the data columns from **sims.zip** as well as:
- *count*: Degree centrality for the article
#### se_count.csv
A processed dataset exclusively used for _number of sampled similar pairs by year analysis_ from the SI. Only treats similar M-F pairs. Consists of the following data columns:
- *year*: Publication year of a paper that was written later
- *count*: Number of M-F pairs in that year
### Codes
The following Python packages were used:
- collections.defaultdict
- itertools
- math
- matplotlib.pyplot
- mpl_toolkits.axes_grid1.inset_locator.inset_axes
- mpl_toolkits.axes_grid1.inset_locator.mark_inset
- networkx
- numpy
- pandas
- random
- random.randint
- scipy.interpolate.BSpline
- scipy.interpolate.interp1d
- scipy.interpolate.make_interp_spline
- scipy.stats
- seaborn
- time
- tqdm
- warnings
#### First_mover_advantage.ipynb
Contains all analyses performed in the main text
#### First_mover_advantage_SI.ipynb
Contains all analyses performed in the supplementary materials
#### First_mover_advantage_SIMILARITY_ALGORITHM.ipynb
Performs the similarity algorithm highlighted in the *Methods* from the main text
