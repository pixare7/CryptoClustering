# CryptoClustering

## Overview
This project uses machine learning techniques to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. 

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
Use unsupervised learning:
   - normalize the data
   - find the best value for k in the scaled dataframe
   - cluster cryptocurrencies with k-means using the scaled dataframe
   - optimize clusters with Principal Component Analysis (PCA)
   - Find the best value for k using the PCA dataframe
   - cluster the cryptocurrencies with k means using the pca dataframe

### Methodology
Detail the approach and methods used to achieve the project's goals.

In the "Methodology" section, you would typically describe the specific approaches, 
techniques, tools, and processes you used to accomplish the project's goals. Here are some examples of what you might include:

1. **Data Collection:**
   - The cryptocurrency data was collected on a CSV file

2. **Data Cleaning:**
   - the StandardScaler() module from scikit-learn was used to normalize the data from the CSV file

3. **Data Transformation:**
   - the StandardScaler() module from scikit-learn was used to normalize the data from the CSV file
   - Principal Component Analysis (PCA) was used to extract the most essential features which account for most variability in the data to later predict the clusters

4. **Exploratory Data Analysis (EDA):**
   - A summary statistics table was created to show the count, mean, standard deviation, min quartiles, and max of the price_change_percentage_24h, price_change_percentage_7d,
       price_change_percentage_14d, price_change_percentage_30d, price_change_percentage_60d, price_change_percentage_200d, price_change_percentage_1y columns. 
   - hvplot.pandas was used to visualize price performance of different crypto currencies over time
   - same library was used to plot elbow curves to determine ethe best k value to use to cluster cryptocurrencies
   - the same library was used to plot the cluster cryptocurrency scatter plots clusters
   
5. **Data Analysis:**
   - A plot of price performance of different crypto currencies over time was used to examine the flucuation of cryptocurrencies over 24 hour, 7 day, 14 day, 30 day, 60 day, 200 day, and one year.  
   - the scatterplots were used to analyze if there is a pattern between cryptocurrencies affected by 24 hour price changes vs 7 hour price changed and cluster them

6. **Modeling and Prediction:**
   - k means model was initialized. the k means model was fitted using teh scaled dataaframe.  then the model was used to predict the clusters to group the cryptocurrencies based on the scaled dataframe
   - the clusters were then optimized with PCA to reduce features to three principal components

7. **Visualization:**
   - A summary statistics table was created to show the count, mean, standard deviation, min quartiles, and max of the price_change_percentage_24h, price_change_percentage_7d,
       price_change_percentage_14d, price_change_percentage_30d, price_change_percentage_60d, price_change_percentage_200d, price_change_percentage_1y columns. 
   - hvplot.pandas was used to visualize price performance of different crypto currencies over time
   - same library was used to plot elbow curves to determine ethe best k value to use to cluster cryptocurrencies
   - the same library was used to plot the cluster cryptocurrency scatter plots clusters

8. **Tools and Libraries:**
    - pandas, hvplot.pandas, from sklearn.cluster import KMeans, from sklearn.decomposition, import PCA from sklearn.preprocessing, StandardScaler, matplotlib.pyplot, seaborn

### Visuals

#### Figure 1: [Cryptocurrencies Over TIme]
![Figure 1](https://github.com/pixare7/CryptoClustering/blob/main/images/fig01.png)

*This plots the price percentage change over time for each cryptocurrency.*

#### Figure 2: [Elbow Curve]
![Figure 2](https://github.com/pixare7/CryptoClustering/blob/main/images/fig02.png)

*The elbow method on the scaled dataframe indicates that the best value for k is 4.*

#### Figure 3: [Elbow Curve Using PCA Data]
![Figure 3](https://github.com/pixare7/CryptoClustering/blob/main/images/fig03.png)

*Using the elbow method on the scaled PCA dataframe also suggests that the best value for k is 4.*

#### Figure 4: [Scatter Plot]
![Figure 4](https://github.com/pixare7/CryptoClustering/blob/main/images/fig04.png)

*The cryptocurrencies were clustered using k=4 on the scaled dataframe.*

#### Figure 5: [Scatter Plot Using PCA Data]
![Figure 5](https://github.com/pixare7/CryptoClustering/blob/main/images/fig05.png)

*The clusters were optimized using PCA.*

## Conclusions

The clustering prediction shows that cryptocurrencies that tend to have larger price changes over 24 hours also tend to have larger price changes over 7 days.

## Future Work
Discuss any potential extensions, improvements, or follow-up projects 
that could build on the work done in this project.
