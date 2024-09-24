# CryptoClustering
Overview
This project aims to cluster cryptocurrencies using K-Means clustering and Principal Component Analysis (PCA) on normalized market data. 

Table of Contents
1. Prepare the Data
2. Find the Best Value for k Using the Scaled DataFrame
3. Cluster Cryptocurrencies with K-means Using the Scaled DataFrame
4. Optimize Clusters with Principal Component Analysis
5. Find the Best Value for k Using the PCA DataFrame
6. Cluster Cryptocurrencies with K-means Using the PCA DataFrame
7. Visualize and Compare the Results

Details
1. Prepare the Data
   
Normalize the Data by using StandardScaler() module from scikit-learn
Create a DataFrame with the scaled data and set the"coin_id" index


2. Find the Best Value for k Using the Scaled DataFrame
   
Create k Values
Calculate Inertia
Plot Elbow Curve to determine the best value for k


3. Cluster Cryptocurrencies with K-means Using the Scaled DataFrame
   
Initialize the K-means model with the best value for k.
Fit the K-means model using the scaled DataFrame
Predict clusters to group the cyrptocurrencies
Create a new column with predicted clusters
Create a scatter plot with:
    X-axis: "price_change_percentage_24h"
    Y-axis: "price_change_percentage_7d"
    Color the points by cluster labels.
    Include the "coin_id" column in the hover_cols parameter.


4. Optimize Clusters with Principal Component Analysis
   
Perform PCA and reduce features to three principal components.
Retrieve the explained variance to determine how much information can be attributed to each principal component. 
Create a new PCA DataFramewith the scaled PCA data and set the "coin_id" index from the original DataFrame 


5. Find the Best Value for k Using the PCA DataFrame
   
Create k Values
Calculate Inertia
Plot Elbow Curve to determine the best value for k


6. Cluster Cryptocurrencies with K-means Using the PCA DataFrame
   
Initialize the K-means model with the best value for k.
Fit the K-means model using the scaled PCA DataFrame
Predict clusters to group the cyrptocurrencies
Create a new column with predicted clusters
Create a scatter plot with:
    X-axis: "PC1"
    Y-axis: "PC2"
    Color the points by cluster labels.
    Include the "coin_id" column in the hover_cols parameter.


7.  Visualize and Compare the Results
   
Create composite plot by using hvPlot and + operator to compare elbow curve of the original scaled DataFrame and the PCA dataFrame
Create composite plot by using hvPlot and + operator to compare cryptocurrency clusters of the original scaled DataFrame and the PCA dataFrame
Analyse the impact of using fewer features to cluster the data using K-Means

Conclusion
The impact of using fewer features to cluster the data using K-means, particularly when applying PCA, generally results to the following:
  - more distinct or simplified PCA clustering as it only emphasizes the most relevant features while the original DataFrame are less defined due to irrelevant features. Having fewer features reduces complexity, which can lead to faster computation times and easier interpretation of the results.
  - Even after reducing features, original and PCA DataFrames still have the same optimal # of clusters from the elbow curve indicates that the inherent structure of the data remains consistent, regardless of lesser features reduction. Having the same optimized K indicates that the clustering structure remains valid across both.
