![Cryptocurrency Analysis](Resources/Crypto.jpg)

## Overview of the Project

The purpose of this project is to assist a client who is interested in offering a new cryptocurrency investment portfolio for its customers. The company has requested a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data is not ideal, so it will need to be processed to fit the machine learning models using unsupervised learning grouping and a clustering algorithm. 

There are four technical analysis deliverables:

Deliverable 1: Preprocessing the Data for PCA
Deliverable 2: Reducing Data Dimensions Using PCA
Deliverable 3: Clustering Cryptocurrencies Using K-means
Deliverable 4: Visualizing Cryptocurrencies Results

## Results

### Deliverable 1: Preprocessing the Data for PCA

The data was preprocessed to eliminate unnecessary data:

- Keep all the cryptocurrencies that are being traded

![Cryptocurrency Traded](Resources/01trading.jpg)

- Keep all the cryptocurrencies that have a working algorithm

![Cryptocurrency Algorithms](Resources/02algorithms.jpg)

- Remove the "IsTrading" column

![Cryptocurrency Trading](Resources/03trading.jpg)

- Remove rows that have at least 1 null value

![Cryptocurrency Drop Nulls](Resources/04dropna.jpg)

- Keep the rows where coins are mined

![Cryptocurrency Coins Mined](Resources/05coinsmined.jpg)

- Create a new DataFrame that holds only the cryptocurrencies names

![Cryptocurrency Names](Resources/06cryptonamed.jpg)

- Drop the 'CoinName' column since it's not going to be used on the clustering algorithm

![Cryptocurrency Drop CoinName](Resources/07dropcoin.jpg)

- Use get_dummies() to create variables for text features

![Cryptocurrency Get Dummies](Resources/08getdummies.jpg)

- Standardize the data with StandardScaler()

![Cryptocurrency StandardScaler](Resources/09scale.jpg)


### Deliverable 2: Reducing Data Dimensions Using PCA

- Using PCA to reduce dimension to three principal components

![Cryptocurrency PCA Components](Resources/2PCA.jpg)

- Create a DataFrame with the three principal components

![Cryptocurrency Component DataFrame](Resources/2DF.jpg)


### Deliverable 3: Clustering Cryptocurrencies Using K-means

- Create an elbow curve to find the best value for K and find the best value for K

![Cryptocurrency Elbow](Resources/3Elbow.jpg)

- Run K-Means with k=4

![Cryptocurrency Kmeans](Resources/3Kmeans.jpg)



### Deliverable 4: Visualizing Cryptocurrencies Results

- Creating a 3D-Scatter with the PCA data and the clusters

![Cryptocurrency 3D Graph](Resources/43D.jpg)

- Create a table with tradable cryptocurrencies

![Cryptocurrency New Table](Resources/4Table.jpg)

- Print the total number of tradable cryptocurrencies

![Cryptocurrency New Table](Resources/4Table.jpg)

- Scaling data to create the scatter plot with tradable cryptocurrencies

![Cryptocurrency Tradeable](Resources/4Tradeable.jpg)

- Create new DataFrame with scaled data, add CoinName and Class columns

![Cryptocurrency Scaled Data](Resources/4Scale.jpg)

![Cryptocurrency New DF](Resources/4NewDf.jpg)

- Create a hvplot.scatter plot using x="TotalCoinsMined" and y="TotalCoinSupply"

![Cryptocurrency Scatterplot](Resources/4Scatter.jpg)

## Summary

The cryptocurrencies were divided into 4 groups, with the majority of the cryptocurrencies falling into groups 0 and 3.