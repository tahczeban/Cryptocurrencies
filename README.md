# Cryptocurrencies
_________________
![image](https://user-images.githubusercontent.com/90135381/157934765-86d3c0ca-d52a-4c0b-89c2-941f011265d8.png)



***RESOURCES:***

***IMAGE:*** image obtained from PNGwing.com 

***DATA:*** crypto_data.csv, crypto_clustering_starter_code.ipynb

***SOFTWARE:*** Anaconda, Jupyter Notebook, Python, VSC

***LIBRARIES:*** Plotly, hvPlot, Scikit-learn, Pandas




_______________
***OVERVIEW:***

This challenge entailed collaberation with Martha, a Senior manager for the Advisory Services team at Accountability Accounting, to assist with preparation of an analysis for an investment bank who wishes to enter the Cryptocurrency market by way of offering a cryptocurrency investment portfolio. A report was compiled addressing which cryptocurrencies are currently available on the market and how they can be grouped together into a classification system for this investment venture. Due to the nature of this project, unsupervised machine learning was deemed the most efficient tool for analysis via a clustering algorithm with corresponding visualizations.


______________
***RESULTS:***


***Deliverable 1: Preprocessing the data for PCA.***

For this first Deliverable, the preprocessing was completed prior to the Principal Component Analysis (PCA) via:
1. the traded cryptocurrencies were kept 
2. the 'IsTrading' column was dropped 
3. null rows were removed  
4. rows with coins that are not being mined were removed 
5. DF with cryptocurrency names was created 
6. the CoinName column was removed 
7. variables for 'Algorithm' and 'ProofType' were created and stored in X DF 
8. the data was standardized with StandardScaler



<img width="1186" alt="D1-CoinName:drop CoinName" src="https://user-images.githubusercontent.com/90135381/157932866-632f8404-02da-46e6-9c36-7b3eddc6fff1.png">


                         FIGURE 1: Removed non-trading Cryptocurrencies and Drop CoinName

***Deliverable 2: Reducing Data Dimensions Using PCA***

Deliverable 2, entailed applying the Principal Component Analysis algorithm: 
1. reducing the X-DF into 3 dimensions 
2. placing this into new DF
3. creating the pcs DF, including the 3 columns PC1, PC2, PC3, which has the index from the crypto_df


<img width="1440" alt="Del2-DF w:3 comp" src="https://user-images.githubusercontent.com/90135381/157932885-c59f0064-8980-4e23-ae0a-bad6ccd81f0f.png">


                         FIGURE 2: PCA Algorith Reducing Dimensions to 3 Principal Componenets


***Deliverable 3: Clustering Cryptocurrencies Using K-means***

This Deliverable included clustering with vizualizations:
1. an elbow curve wa created with hvplot to find the optimal value for K 
2. the K-means algorithm was implemented to predict the K clusters for the cryptocurrency data
3. the crypto_df and pcs_df were concatenated into the new clustered_df  
4. a CoinName column was added
5. a class column was also added to hold the predictions with the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC1, PC2, PC3, CoinName, Class


<img width="1313" alt="Del3-clustered DF" src="https://user-images.githubusercontent.com/90135381/157932927-fad1cf71-a2ad-4c3a-8264-3f7da071971a.png">


                        FIGURE 3: Concatenated Clustered Dataframe with added CoinName and Class

<img width="1139" alt="Del3-Elbow curve" src="https://user-images.githubusercontent.com/90135381/157932938-648d0c63-eeb2-4a58-a5d1-4815f9d5d16c.png">


                        FIGURE 4: Elbow Curve Depicting Best K Value for Predictions

***Deliverable 4: Vizualize Cryptocurrencies Results***

In this last Deliverable, the results were transformed into relatable vizualizations:
1. plotly express/hvplot were utilized to create a 3D scatter plot for visualizing the distinct groups corresponding to the 3 principal components
2. CoinName' and 'Algorithm' columns were added to the hover_name and hover_data parameters to show the data points
3. a table displaying the tradable cryptocurrencies with hvplot.table() was created 
4. the total number of tradable cryptocurrencies was printed
5. a DF containing clustered_df index, the scaled data and the columns 'CoinName' and 'Class' was created
6. Finally, a scatterplot with X-axis='TotalCoinsMined' and Y-axis='TotalCoinSupply', with ordered data by 'Class', with hover point showing 'CoinName' was created


<img width="1136" alt="Del4-3d scatter with hovername" src="https://user-images.githubusercontent.com/90135381/157932972-b9a868fd-e668-4da7-b4fe-157caee1961c.png">


                        FIGURE 5: 3D Scatterplot with hover name and data for the 3 Clusters

<img width="1176" alt="Del4-hvplot table()" src="https://user-images.githubusercontent.com/90135381/157932992-ec791b73-cf2c-463c-9831-e8b4dc3a4ec7.png">


                        FIGURE 6: hvplot Table Illustrating tradable Cryptocurrencies

<img width="1172" alt="Del4-DF with added CoinName and Class" src="https://user-images.githubusercontent.com/90135381/157932980-6a3b29cf-9d6e-43ad-b582-034960df04c1.png">


                        FIGURE 7: Dataframe with added CoinName and Class

<img width="1171" alt="Del4-Scatterplot" src="https://user-images.githubusercontent.com/90135381/157933002-0a822326-3e57-4d3b-97ef-f47ea31f1da1.png">

                        FIGURE 8: Scatter plot with TotalCoinsMined and TotalCoinSupply, by Class

______________
***SUMMARY:***

In conclusion, unsupervised machine learning was successfull in determining the data required for the bank to implement its novel portfolio implementation. Additionally, vizualization libraries were utilized to effectively convey the requested information as follows:
1. the elbow curve depicting the best value for K for the K-means algorithm for cryptocurrency cluster predictions
2. a 3D scatterplot plotting the 3 clusters, including hover name and data
3. the hvplot.table() listing clustered PCA data and in tabular format
4. a scatterplot illustrating TotalCoinsMined(x) and TotalCoinSupply(y) by Class

________________
***REFERENCES:*** BSC, Google, StackOverFlow, GitHub

