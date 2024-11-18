# Crypto Clustering Project

## Overview

This project aims to explore unsupervised machine learning techniques to analyze cryptocurrency market data. The goal is to determine if 24-hour and 7-day price changes influence the clustering of cryptocurrencies. We will use K-means clustering, combined with Principal Component Analysis (PCA), to group cryptocurrencies and visualize their relationships.

## Project Steps

### 1. Data Preparation

    File Loaded: crypto_market_data.csv
    Initial Tasks:
        Load data into a DataFrame.
        Generate summary statistics.
        Visualize the data.

### 2. Data Normalization

    Scaling:
        Used StandardScaler() from scikit-learn to normalize the data.
        Created a new DataFrame with scaled values, retaining coin_id as the index.

### 3. Elbow Method for Optimal k

    Goal: Determine the optimal number of clusters.
    Steps:
        Tested values of k from 1 to 11.
        Calculated inertia for each k.
        Plotted an elbow curve to visually identify the optimal k.

### 4. K-means Clustering on Scaled Data

    Model Initialization: K-means with optimal k.
    Tasks:
        Predicted clusters for scaled data.
        Added cluster labels to the DataFrame.
        Visualized clusters using hvPlot (scatter plot of 24-hour vs. 7-day price changes).

### 5. Principal Component Analysis (PCA)

    Purpose: Reduce dimensionality to three principal components.
    Tasks:
        Calculated explained variance for each component.
        Created a new DataFrame using the PCA-transformed data.
        Answered: What is the total explained variance of the three principal components?

### 6. Elbow Method with PCA Data

    Repeated the elbow method on PCA-transformed data.
    Compared the optimal k with and without PCA.

### 7. K-means Clustering on PCA Data

    Model Initialization: K-means with optimal k on PCA data.
    Tasks:
        Predicted clusters.
        Visualized clusters (scatter plot of PC1 vs. PC2).
        Answered: What is the impact of using fewer features on clustering?

## Key Questions Addressed

    Best value for k:
        From both the original and PCA-transformed data.
    Impact of PCA:
        Compared clustering results with fewer features (principal components).

## Technologies Used

    Python Libraries:
        pandas and numpy for data manipulation.
        scikit-learn for scaling, K-means, and PCA.
        hvPlot for interactive visualizations.
