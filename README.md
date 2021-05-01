# Cryptocurrencies
## Purpose
The purpose of this analysis was to create a cryptocurrency investment portfolio using unsupervised machine learning. The data included different currencies with their corresponding features such as coin supply, total coins mined, proof type etc. The dimensionality of the features were reduced to 3 using Principal Component Analysis and then the K means algorithm was used to group the currencies into four categories.  
The machine learning library used here is sklearn.

## Analysis
These are the steps I followed to perform the analysis:
 1. The data was cleaned using Pandas by dropping null values, filtering the tradeable currencies etc 
  <img src = "https://github.com/Kee2u/Cryptocurrencies/blob/main/Pictures/clean_data.PNG?raw=true">
 2. The get_dummies() function was used to create variables for text features
 3. The data was scaled using sklearn's StandardScaler() function and then the dimensions were reduced to 3 using sklearn's PCA algorithm
  <img src = "https://github.com/Kee2u/Cryptocurrencies/blob/main/Pictures/PCA.PNG?raw=true">
 4. An elbow curve was generated using the reduced dataset to determine the best number of clusters.
  <img src = "https://github.com/Kee2u/Cryptocurrencies/blob/main/Pictures/elbow_curve.PNG?raw=true">
 5. Finally Sklearn's KMeans algorithm was implemented to group the currencies into four clusters (or classes).

## Results
Of all the classes, class two seems to have the highest variance in amount of coins mined. Classes 0, 2 and 3 have similar values of total coins supplied. The outlier is the currency that belongs to class one. It has both a high amount of coins mined and coins supplied. 
<img src = "https://github.com/Kee2u/Cryptocurrencies/blob/main/Pictures/3Dplot.PNG?raw=true" width = "800">
<img src = "https://github.com/Kee2u/Cryptocurrencies/blob/main/Pictures/2Dplot.PNG?raw=true" width = "800">
## Future Analysis 
The features such as Proof type and Algorithm had a factor to play in the creation of the clusters as well. To get an idea of the role they had to play, we can look at their values within each cluster to search for patterns.
