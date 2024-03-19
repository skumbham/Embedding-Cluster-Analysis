# Clustering Word Embeddings

This repository presents a thorough analysis demonstrating the clustering of word embeddings using various machine learning techniques. The aim is to reveal intrinsic thematic structures within a text corpus, employing dimensionality reduction and clustering methods for insightful data exploration.

## Project Overview

The analysis proceeds through the following steps:

### Step 1: Load the Newsgroups Data
- **Library Imports**: Utilizes `warnings` to suppress future warnings and `fetch_20newsgroups` from `sklearn.datasets`.
- **Warnings Configuration**: Employs `warnings.simplefilter` to improve output readability.
- **Category Selection**: Defines a subset of categories for focused analysis.
- **Data Fetching**: Loads data using `fetch_20newsgroups` with selected categories.
- **Data Access**: Displays the first document and its target, alongside the dataset size.

### Step 2: Vectorize the Data
- **Vectorizer Import**: Incorporates `TfidfVectorizer` from `sklearn.feature_extraction.text`.
- **Vectorizer Initialization**: Creates a `TfidfVectorizer` instance, excluding English stop words.
- **Feature Extraction**: Identifies top N terms based on TF-IDF scores.

### Step 3: Integrate GloVe Vectors
- **GloVe Loading**: Reads the GloVe vector file, constructing a word to vector mapping.
- **Term Filtering**: Associates the top N TF-IDF terms with their GloVe vectors, omitting unmatched terms.

### Step 4: Dimensionality Reduction and Clustering
- **Apply t-SNE and PCA**: Reduces GloVe vector dimensionality for better visualization and clustering.
- **Clustering**: Utilizes KMeans and Hierarchical Agglomerative Clustering (HAC) on the reduced vectors, including visualization.

### Step 5: Evaluate Clustering Performance
- **Silhouette Scores**: Computes these scores to gauge the clustering effectiveness.

### Step 6: Optimize HAC Parameters
- **Parameter Exploration**: Adjusts HAC parameters, computing silhouette scores to find the optimal settings.

### Step 7: Integrate HDBSCAN for Advanced Clustering
- **HDBSCAN Implementation**: Applies this algorithm post-PCA and UMAP reduction, assessing the outcomes using silhouette and Davies-Bouldin scores.

### Step 8: Additional Exploration with PCA, KMeans, and HAC
- **Extended Analyses**: Executes further clustering analyses with PCA, KMeans, and HAC, supported by evaluations and visualizations.

### Step 9: Cluster Visualization
- **Plot Generation**: Visualizes the clustering results, elucidating data grouping and thematic insights.
