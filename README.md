# Unsupervised Machine Learning for Myopia Prediction

This repository contains the analysis and machine learning model used to explore clustering patients based on characteristics that may influence myopia (nearsightedness). The project applies unsupervised learning techniques to identify patterns in the data that could provide insights into different patient subgroups. 

## Project Overview

The goal of this project was to apply unsupervised learning to the provided medical dataset in order to determine if patients can be grouped into distinct clusters based on their characteristics. This analysis is performed in the context of predicting myopia (nearsightedness), but the task focuses on unsupervised clustering rather than supervised prediction.

### Key Steps Taken:
1. **Data Preprocessing**: The dataset was cleaned and standardized to remove any biases before applying machine learning algorithms.
2. **Dimensionality Reduction**: PCA (Principal Component Analysis) was used to reduce the number of features while preserving 90% of the data variance.
3. **Cluster Analysis**: K-means clustering was performed to identify potential clusters in the data. An elbow plot was used to determine the optimal number of clusters.
4. **Visualization**: t-SNE was applied to visualize the dimensionality reduction and inspect the distinctness of clusters.

## Final Analysis

Through the use of PCA and K-means clustering, it was determined that the dataset can be split into **3 distinct clusters**. 
- Using two principal components (PCA=2), 38% of the data variance is explained, while increasing to three components (PCA=3) captures 47.24% of the variance.
- A clear grouping of patient characteristics was observed, suggesting that the clustering technique reveals underlying patterns in the data.
- Further investigation into which features are most important for predicting myopia may help reduce the number of variables and potentially improve the clustering model.

## Project Breakdown

### Part 1: Data Preparation
- Read the dataset from `myopia.csv`.
- Removed the "MYOPIC" target column to ensure an unbiased unsupervised learning process.
- Standardized the dataset to ensure all features contribute equally to the analysis.

### Part 2: Dimensionality Reduction
- Applied PCA to reduce the number of features while retaining 90% of the variance.
- Further reduced the data's dimensionality using t-SNE and visualized the results with a scatter plot to check for distinct clusters.

### Part 3: Cluster Analysis with K-means
- Generated an elbow plot to determine the optimal number of clusters.
- Performed K-means clustering on the dataset, testing for clusters between 1 to 10 and identifying the elbow point.

### Part 4: Recommendation
Based on the analysis:
- Patients can indeed be clustered into **3 distinct groups** based on the available characteristics.
- These clusters can potentially be analyzed separately to improve myopia prediction models.

## Files Included

- `myopia.csv`: The raw dataset containing patient characteristics.
- `myopia_pca_tsne_kmeans.ipynb`: Jupyter notebook containing the analysis, including code for PCA, t-SNE, and K-means clustering.

## Installation

To run the code and analysis in this repository:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/unsupervised-machine-learning.git
