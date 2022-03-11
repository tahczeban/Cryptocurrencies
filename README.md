# Cryptocurrencies
_________________
***RESOURCES:***


***DATA:*** crypto_data.csv, crypto_clustering_starter_code.ipynb

***SOFTWARE:*** Anaconda, Jupyter Notebook, Python, VSC

***LIBRARIES:*** Plotly, hvPlot, Scikit-learn, Pandas




_______________
***OVERVIEW:***


Work with Martha , Senior manager for Advisory Services team at Accountability Accountingto prepare an analysis for an investment bank who wish to enter the Cryptocurrency market by way of offering a cryptocurrency investment portfolio
report pertaining to which cryptocurrencies are on the market and how they can be grouped together into a classification system
with K-means algorithm, which groups similar data into clusters
implement PCA (principal component analysis)




______________
***RESULTS:***
_

***Deliverable 1: Preprocessing the data for PCA.***

keep traded cryptocurrencies. drop 'IsTrading' column, remove null rows, remove rows with coins that are not being mined, DF with ccryptocurrency names, remove CoinName, create variables for 'Algorithm' and 'ProofType' and store in X DF, standardize the data with StandardScaler

<img width="1186" alt="D1-CoinName:drop CoinName" src="https://user-images.githubusercontent.com/90135381/157932866-632f8404-02da-46e6-9c36-7b3eddc6fff1.png">


***Deliverable 2: Reducing Data Dimensions Using PCA***

apply Principal Component Analysis algorithm and reduce X-DF into 3 dimensions and place into new DF 
create pcs DF and include the 3 columns PC1, PC2, PC3, which has the index from the crypto_df


<img width="1440" alt="Del2-DF w:3 comp" src="https://user-images.githubusercontent.com/90135381/157932885-c59f0064-8980-4e23-ae0a-bad6ccd81f0f.png">




***Deliverable 3: Clustering Cryptocurrencies Using K-means***


create elbow curve with hvplot to find the optimal value for K 
usethe K-means algorithm to predict the K clusters for the cryptocurrency data
concatenate crypto_df and pcs_df into new clustered_df  and add CoinName column
add class column to hold the predictions with the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC1, PC2, PC3, CoinName, Class


<img width="1313" alt="Del3-clustered DF" src="https://user-images.githubusercontent.com/90135381/157932927-fad1cf71-a2ad-4c3a-8264-3f7da071971a.png">



<img width="1139" alt="Del3-Elbow curve" src="https://user-images.githubusercontent.com/90135381/157932938-648d0c63-eeb2-4a58-a5d1-4815f9d5d16c.png">


***Deliverable 4: Vizualize Cryptocurrencies Results***

utilize plotly express/hvplot to create a 3D scatter plot to visualize the distinct groups correspondint to the 3 principal components
add 'CoinName' and 'Algorithm' columns to the hover_name and hover_data parameters to show the data points
create a table displaying the tradable cryptocurrencies with hvplot.table() and print the total number of tradable cryptocurrencies
create a DF containing clustered_df index, the scaled data and the columns 'CoinName' and 'Class'
create a scatterplot with X-axis='TotalCoinsMined' and Y-axis='TotalCoinSupply', with ordered data by 'Class', with hover point showing 'CoinName'


<img width="1136" alt="Del4-3d scatter with hovername" src="https://user-images.githubusercontent.com/90135381/157932972-b9a868fd-e668-4da7-b4fe-157caee1961c.png">


<img width="1176" alt="Del4-hvplot table()" src="https://user-images.githubusercontent.com/90135381/157932992-ec791b73-cf2c-463c-9831-e8b4dc3a4ec7.png">



<img width="1172" alt="Del4-DF with added CoinName and Class" src="https://user-images.githubusercontent.com/90135381/157932980-6a3b29cf-9d6e-43ad-b582-034960df04c1.png">




<img width="1171" alt="Del4-Scatterplot" src="https://user-images.githubusercontent.com/90135381/157933002-0a822326-3e57-4d3b-97ef-f47ea31f1da1.png">

______________
***SUMMARY:***


In conclusion, unsupervised machine learning wa ssuccessfulll in determining the data required for the bank to implement its portfolio
TotalCoinsMined and TotalCoinSupply with educational visualizations




________________
***REFERENCES:*** BSC, Google, StackOverFlow, GitHub

