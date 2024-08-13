
<h1 align="center">Unsupervised Learning with Python </h1>
<h3 align="center">Predict if cryptocurrencies are affected by 24-hour or 7-day price changes</h1>
<div align="center">
	<img src="Images/CurrencyIcon.png">
</div>


## Background.
Cryptocurrencies have become a significant part of the global financial landscape, 
known for their high volatility and potential for substantial gains or losses over short periods. 
Unlike traditional financial assets, the value of cryptocurrencies can fluctuate wildly within hours or days, 
influenced by a range of factors including market sentiment, news, regulatory changes, and technological developments.
In this project, we aim to explore the underlying patterns in cryptocurrency price movements using unsupervised learning techniques.
Specifically, the focus is on determining whether the prices of various cryptocurrencies are influenced by their 24-hour or 7-day price changes. 
By applying clustering algorithms and other unsupervised learning methods, we can group cryptocurrencies with similar price behaviors and analyze the factors that may contribute to these patterns.

## Data sources.
- [crypto_market_data](Resources/crypto_market_data.csv)

## Unsupervised model.
- [KMeans](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
- [Principal component analysis (PCA).](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html#sklearn.decomposition.PCA)

## Process  
- Prepare the Data
  - Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
- Find the Best Value for k Using the original scaled dataFrame.
  - [Elbow curve before the optimization](images/elobow_before_Optimization.png)
- Clusters Cryptocurrencies with K-means Using the original scaled Data.
  - [Scatter plot chart for the original data](images/original_scatter.png) 
- Optimize Clusters with Principal Component Analysis.
  - [Elbow after the optimization data](Images/elobow_after_Optimization.png)  
- Cluster Cryptocurrencies with K-means Using the PCA Data.
  - [Clusters Cryptocurrencies with K-means Using the optimized scaled Data](Images/Optimization_scatter.png)
- Visual comparison of the graphs before and after the optimization. 
  - [Elbow graphs comparison](Images/elobowComparison.png)
  - [Scatter plot graphs comparison](Images/scatterComparison.png)

## Summary.
- What is the best value for k?  : The best value for the k is 4 in before and after the data optimization.
- What is the total explained variance of the three principal components? : The total explained variance of the three principal components is approximately 0.895 or 89.5%.
- After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?  : With fewer features, the clusters are more compact and separable.
- Conclusion of the two models  : This modeling (Optimize Clusters with Principal Component Analysis) more accurate If the selected features are highly relevant for clustering.In this analysis total explained variance of the three principal components is approximately 0.895 or 89.5%.

