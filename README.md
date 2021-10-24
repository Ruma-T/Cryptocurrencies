# Cryptocurrencies
### 
We'll use unsupervised machine learning to analyze data on the cryptocurrencies. To introuce a new cryptocurrencies investment portfolio for the customers, we have to create a report that includes how the available trading market cryptocurrencies could be grouped to create a classification system for this new investment.
clustering algorithm and visualization will be used to help determine investment groupings of this product.

### 
We used crypto_data.csv for data analysis.


### Deliverable 1: Preprocessing the Data for PCA

Read in the crypto_data.csv to the Pandas DataFrame named crypto_df.
Dropped the IsTrading column.
Removed rows that have at least one null value.
Filtered the crypto_df DataFrame so it only has rows where coins have been mined.
Created a new DataFrame that holds only the cryptocurrency names, and use the crypto_df DataFrame index as the index for this new DataFrame.
Removed the CoinName column from the crypto_df DataFrame since it's not going to be used on the clustering algorithm.

![png_18mod1](https://github.com/Ruma-T/Cryptocurrencies/blob/main/Resources/18mod1.PNG)

Used the get_dummies() method to create variables for the two text features, Algorithm and ProofType, and stored the resulting data in a new DataFrame named X.
Used the StandardScaler fit_transform() function to standardize the features from the X DataFrame.

### Deliverable 2: Reducing Data Dimensions Using PCA

Created a new DataFrame named pcs_df that includes the following columns, PC 1, PC 2, and PC 3, and uses the index of the crypto_df DataFrame as the index.

![png_18mod2](https://github.com/Ruma-T/Cryptocurrencies/blob/main/Resources/18mod2.PNG)



### Deliverable 3: Clustering Cryptocurrencies Using K-means
The K-means algorithm is used to cluster the cryptocurrencies using the PCA data
An elbow curve is created using hvPlot to find the best value for K 
Predictions are made on the K clusters of the cryptocurrencies’ data
A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class 

![png_18mod3](https://github.com/Ruma-T/Cryptocurrencies/blob/main/Resources/18mod3.PNG)



### Deliverable 4: Visualizing Cryptocurrencies Results
Created a 3D scatter plot using the Plotly Express scatter_3d() function to plot the three clusters from the clustered_df DataFrame.
Added the CoinName and Algorithm columns to the hover_name and hover_data parameters, respectively, so each data point shows the CoinName and Algorithm on hover.

![png_18mod4](https://github.com/Ruma-T/Cryptocurrencies/blob/main/Resources/18mod4.PNG)






![png_18mod6](https://github.com/Ruma-T/Cryptocurrencies/blob/main/Resources/18mod6.PNG)





![png_18mod7](https://github.com/Ruma-T/Cryptocurrencies/blob/main/Resources/18mod7.PNG)


