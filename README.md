[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/lauFYeeP)
# DS340H Capstone: Identifying Business-Oriented #SAHM Creators on TikTok
This repository contains the code for the final data science capstone that explores how to computationally identify business-oriented/entrepreneurial stay-at-home mom (SAHM) creators on TikTok. The project compares multiple identification strategies—heuristic, unsupervised, and supervised—using hashtag-based and text-based signals.

The primary goal is to evaluate which approach most reliably identifies entrepreneurial creators, rather than to make claims about platform level inequality or causal outcomes.

Research Question:
How can we identify business-oriented and entrepreneurial #sahm creators on TikTok using hashtag-based features, and which modeling approach provides the best predictive accuracy?

## Data
The project uses a large TikTok dataset filtered around the hashtag #SAHM. Raw data are not included in the repository due to size constraints.

Key processed data files include:

`user_post_summary.csv`:
Per-user summary statistics (e.g., total posts, activity span)

`us_hashtags_splintered.csv`
Post-level hashtag data expanded so each row corresponds to a single hashtag use

`hashtags_more_than_30_users.csv`
Filtered hashtag vocabulary used for TF-IDF feature construction

`business_mom_labels.csv`
Manually labeled subset of creators used for evaluation

`user_business_three_methods.csv / user_business_four_methods.csv`
Final prediction outputs from the modeling pipeline

All usernames are treated as identifiers only and are not manually inspected for reproduction. To protect the privacy of

## How to Run the Code

1. Open the main notebook and run cells top to bottom.

2. Required packages include:
- pandas, numpy
- scikit-learn
- sentence-transformers
- duckdb

3. All file paths are relative to the project root.

4. Final outputs are written to CSV files in the data/ directory.


## Notes and Limitations
- The labeled dataset is intentionally small and used only for method comparison, not population-level inference.
- Results should be interpreted as evidence about model performance, not definitive classifications of individual creators.
- Some figures are designed specifically for poster presentation rather than publication.