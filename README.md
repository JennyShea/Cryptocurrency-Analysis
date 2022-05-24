Using data from CryptoCompare, identify which cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system.
Data Preparation
Read crypto_data.csv into Pandas. 
![image](https://user-images.githubusercontent.com/86893003/170097320-e537025e-ad14-4a47-b719-3a2c35b13ab9.png)
 
Discard all cryptocurrencies that are not being traded and drop the IsTrading column from the dataframe.
Remove all rows that have at least one null value.
Filter for the cryptocurrencies that have been mined. 
Delete the CoinName from the original dataframe as it is not numeric.
![image](https://user-images.githubusercontent.com/86893003/170097387-cec9d745-df73-4a60-b7e8-3d92f4779bb5.png)

Convert the remaining features with text values, Algorithm and ProofType, to numerical data using Pandas to create dummy variables.
![image](https://user-images.githubusercontent.com/86893003/170097426-a2682b86-4e30-4ed4-aa5e-86bc942719c2.png)

Standardize your dataset so that columns that contain larger values do not unduly influence the outcome.
![image](https://user-images.githubusercontent.com/86893003/170097554-a6f5fcce-2363-448d-be3b-f2f4d3f79941.png)

Dimensionality Reduction
![image](https://user-images.githubusercontent.com/86893003/170097676-bd0aaec0-9fce-43e9-b39f-33b3c78794a4.png)
 
Next, further reduce the dataset dimensions with t-SNE and visually inspect the results. In order to accomplish this task, run t-SNE on the principal components: the output of the PCA transformation. Then create a scatter plot of the t-SNE output. Observe whether there are distinct clusters or not.
![image](https://user-images.githubusercontent.com/86893003/170097718-2f18f161-ec74-4c74-88b4-ac8184763aea.png)
 
Cluster Analysis with k-Means
Create an elbow plot to identify the best number of clusters. Use a for-loop to determine the inertia for each k between 1 through 10. Determine, if possible, where the elbow of the plot is, and at which value of k it appears.
![image](https://user-images.githubusercontent.com/86893003/170097757-a9ef85a4-fbfc-43c9-9638-da706bfe1dbf.png)
![image](https://user-images.githubusercontent.com/86893003/170097802-098ea830-d112-46cf-8c87-d2b5ca32da99.png)
 
Recommendation
Based on the T-SNE plot it appears that the cryptocurrencies currently trading on the market can be grouped into one large cluster and two smaller ones.
