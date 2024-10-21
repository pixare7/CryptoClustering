# CryptoClustering

## Overview
This project utilizes machine learning techniques, specifically clustering, to analyze the price behavior of cryptocurrencies over short-term (24-hour) and mid-term (7-day) periods. 
By grouping cryptocurrencies based on their price changes, we can identify patterns that help predict future price movements. 
This analysis is crucial for investors seeking to make informed decisions about cryptocurrency investments, particularly Bitcoin, by understanding how short- and mid-term fluctuations might affect future performance.

## Table of Contents
1. [Overview](#overview)
2. [Project Details](#project-details)
   - [Goals](#goals)
   - [Methodology](#methodology)
   - [Visuals](#visuals)
3. [Conclusions](#conclusions)
4. [Future Work](#future-work)

## Project Details

### Goals
The primary goal is to use unsupervised learning techniques to:
   - Normalize the data.
   - Identify the optimal number of clusters (k) for the scaled dataset.
   - Cluster cryptocurrencies using k-means on the scaled dataset.
   - Optimize the clustering using Principal Component Analysis (PCA).
   - Identify the best k value using the PCA-transformed data.
   - Cluster cryptocurrencies based on the PCA-reduced data.

### Methodology
This section outlines the steps taken to achieve the project goals:

1. **Data Collection:**
   - Cryptocurrency data was collected in a CSV file.

2. **Data Preprocessing:**
   - The `StandardScaler` from scikit-learn was used to normalize the data, ensuring all features have a similar scale.

3. **Dimensionality Reduction with PCA:**
   - PCA was applied to extract the most important features, reducing the data to key components that account for the majority of variance.

4. **Exploratory Data Analysis (EDA):**
   - Summary statistics were generated to provide insights into key cryptocurrency metrics (e.g., 24-hour, 7-day, 30-day price changes).
   - `hvplot.pandas` was used for visualizing cryptocurrency price performance over time.
   - Elbow curves were plotted to determine the optimal number of clusters (k) for both the scaled and PCA-transformed data.
   - Scatter plots were generated to visualize the clustering results.

5. **Clustering and Model Analysis:**
   - The k-means algorithm was implemented, and the scaled data was used to fit the model and predict clusters.
   - PCA was applied to further optimize the clustering by reducing the feature space to three principal components, improving the model’s interpretability.

6. **Tools and Libraries:**
   - Key libraries used: `pandas`, `hvplot.pandas`, `scikit-learn` (for KMeans, PCA, and StandardScaler), `matplotlib.pyplot`, and `seaborn`.

### Visuals

#### Figure 1: Cryptocurrency Price Changes Over Time
![Figure 1](https://github.com/pixare7/CryptoClustering/blob/main/images/fig01.png)

*This plot shows the percentage price change over time for each cryptocurrency.*

#### Figure 2: Elbow Method for Scaled Data
![Figure 2](https://github.com/pixare7/CryptoClustering/blob/main/images/fig02.png)

*The elbow method applied to the scaled data indicates that the optimal number of clusters (k) is 4.*

#### Figure 3: Elbow Method for PCA-Transformed Data
![Figure 3](https://github.com/pixare7/CryptoClustering/blob/main/images/fig03.png)

*The elbow method applied to the PCA-transformed data also suggests that the optimal value for k is 4.*

#### Figure 4: Cryptocurrency Clusters (Scaled Data)
![Figure 4](https://github.com/pixare7/CryptoClustering/blob/main/images/fig04.png)

*Cryptocurrencies clustered using k=4 on the scaled data.*

#### Figure 5: Optimized Clusters (PCA-Transformed Data)
![Figure 5](https://github.com/pixare7/CryptoClustering/blob/main/images/fig05.png)

*Clusters optimized using PCA, reducing the features to three principal components.*

## Conclusions
- The clustering analysis reveals that cryptocurrencies with significant 24-hour price changes often display similar behavior over 7 days, providing insights that can help investors, particularly in Bitcoin, make more informed decisions about future price movements.
- Principal Component Analysis (PCA) improved cluster clarity by highlighting key features, offering deeper insights into price patterns.

## Future Work
Future improvements could include:
   - Analyzing additional time periods or features to further understand cryptocurrency trends.
   - Implementing a more advanced model that incorporates real-time data for ongoing predictions.
