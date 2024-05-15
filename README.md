# Semantic Analysis of Lithium-Ion Battery Patents Using Text Mining and Machine Learning

Welcome to the repository of my thesis project.


### Quick-Guide for the Repository:
df_lemma_dropped.ipynb: data preprocessing; saves the working dataframe for the main part of the thesis as a CSV file.

descriptives.ipynb: code to obtain the descriptive statistics reported in the results section of the thesis.

time_period_analysis_(plots).ipynb: includes several plots of structured data over time. Only the first plot is shown in the paper.

demonstration_simplified.ipynb: code to reproduce the simplified example of the figure in the method section.

Due to RAM limitations, the main code has been split up into several Jupyter Notebooks:

get_tfidf_dummy.ipynb: makes word pair variables and applies the specified filters, saving results to a CSV file.

get-accepted-sentences-qualitative-analysis.ipynb: extracts sentences in which word pair co-occurrences co-appear and saves them to XLSX files; also, the average feature importances are plotted.

1920-2016_BorutaShap_HDBSCAN_UMAP_viz.ipynb: Boruta-SHAP for 1920-2016 periods with UMAP-assisted HDBSCAN plots.

2017-2023_BorutaShap.ipynb: Boruta-SHAP for 2017-2023 time period.


