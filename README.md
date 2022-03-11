# Cryptocurrencies
_________________
***RESOURCES:***
________________

***DATA:*** crypto_data.csv, crypto_clustering_starter_code.ipynb

***SOFTWARE:*** Anaconda, Jupyter Notebook, Python, VSC

***LIBRARIES:*** Plotly, hvPlot, Scikit-learn, Pandas




_______________
***OVERVIEW:***
_______________

Work with Martha , Senior manager for Advisory Services team at Accountability Accountingto prepare an analysis for an investment bank who wish to enter the Cryptocurrency market by way of offering a cryptocurrency investment portfolio
report pertaining to which cryptocurrencies are on the market and how they can be grouped together into a classification system
with K-means algorithm, which groups similar data into clusters
implement PCA (principal component analysis)




______________
***RESULTS:***
______________

***Deliverable 1: Preprocessing the data for PCA.***

keep traded cryptocurrencies. drop 'IsTrading' column, remove null rows, remove rows with coins that are not being mined, DF with ccryptocurrency names, remove CoinName, create variables for 'Algorithm' and 'ProofType' and store in X DF, standardize the data with StandardScaler



***Deliverable 2: Reducing Data Dimensions Using PCA***

apply Principal Component Analysis algorithm and reduce X-DF into 3 dimensions and place into new DF 
create pcs DF and include the 3 columns PC1, PC2, PC3, which has the index from the crypto_df


***Deliverable 3: Clustering Cryptocurrencies Using K-means***


create elbow curve with hvplot to find the optimal value for K 
usethe K-means algorithm to predict the K clusters for the cryptocurrency data
concatenate crypto_df and pcs_df into new clustered_df  and add CoinName column
add class column to hold the predictions with the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC1, PC2, PC3, CoinName, Class


***Deliverable 4: Vizualize Cryptocurrencies Results***

utilize plotly express/hvplot to create a 3D scatter plot to visualize the distinct groups correspondint to the 3 principal components
add 'CoinName' and 'Algorithm' columns to the hover_name and hover_data parameters to show the data points
create a table displaying the tradable cryptocurrencies with hvplot.table() and print the total number of tradable cryptocurrencies
create a DF containing clustered_df index, the scaled data and the columns 'CoinName' and 'Class'
create a scatterplot with X-axis='TotalCoinsMined' and Y-axis='TotalCoinSupply', with ordered data by 'Class', with hover point showing 'CoinName'





______________
***SUMMARY:***
______________






________________
***REFERENCES:*** BSC, Google, StackOverFlow, GitHub
_________________
