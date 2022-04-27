Create a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system.


Process the raw data to fit an unsupervised machine learning model. Use several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. You will use data visualization to share your findings. 


Data Preparation


Read crypto_data.csv into Pandas. The dataset was obtained from CryptoCompare.


Discard all cryptocurrencies that are not being traded and drop the IsTrading column from the dataframe.


Remove all rows that have at least one null value.


Filter for cryptocurrencies that have been mined.


Delete the CoinName from the original dataframe as it is not numeric. 


Convert the remaining features with text values, Algorithm and ProofType, to numerical data using Pandas to create dummy variables. 


Standardize your dataset so that columns that contain larger values do not unduly influence the outcome.



Dimensionality Reduction


Creating dummy variables above dramatically increased the number of features in the dataset. Perform dimensionality reduction with PCA. Rather than specify the number of principal components when you instantiate the PCA model, it is possible to state the desired explained variance. For this project, preserve 90% of the explained variance in dimensionality reduction. 


Next, further reduce the dataset dimensions with t-SNE and visually inspect the results. In order to accomplish this task, run t-SNE on the principal components: the output of the PCA transformation. Then create a scatter plot of the t-SNE output. Observe whether there are distinct clusters or not.



Cluster Analysis with k-Means

Create an elbow plot to identify the best number of clusters. Use a for-loop to determine the inertia for each k between 1 through 10. Determine, if possible, where the elbow of the plot is, and at which value of k it appears.


Recommendation

Based on the T-SNE plot it appears that the cryptocurrencies currently trading on the market can be grouped into one large clusster and two smaller ones. 
