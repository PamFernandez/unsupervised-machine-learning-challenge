### unsupervised-machine-learning-challenge
# Cryptocurrency Clusters

### This assignment was to determine whether the cryptocurrencies on the trading market can be grouped to create a classification system.
----------------------------
----------------------------

## Process
I was given a CSV file that I read into Pandas. This file contained numerous cryptocurrencies with their names, abbreviations, trading status, proof type, number of coins mined, and the total coin supply.
<br>
<br>
I preprocessed the data by:
    <ul><li> dropping all the cryptocurrencies that are not currently being traded
    <li> removing all the rows that have null values
    <li> dropping all cryptocurrencies that have not been mined
    <li> creating a dataframe that has only numeric data in it
    <li> standardizing the data by using the StandardScaler</ul>
<br>
I then used PCA (principal component analysis) to reduce the dimensionality of my data. I created a model that would explain approximatley 90% of the variance. This reduced the number of features in my data from 98 to 74.

To further reduce the dimensions of the dataset I used t-SNE (t-distributed stochastic neighbor embedding) and created a plot to visually inspect the results. My visual observation is that this statistical method <u>does not</u> produce the clusters that we were hoping would indicate the cryptocurrencies could be grouped.

In another effort to create clusters I created a model using k-Means. I used a for loop and a range to find the best value for k and plotted the results. There was no clear elbow to the plot and this method did not yield the information we needed to know how many clusters the data could be grouped into (if any).
<br>
<br>
<b>Recommendation: Using the information that we have created so far in the project, we cannot cluster these cryptocurrencies together.

This does not mean that the cryptocurrency data we've been given cannot be grouped into clusters, it only means that we may need to look at how we preprocessed our data or we may need to use a different algorithm. It is still possible, however, that this data is un-clusterable. </b>

## My Code
* VSCode: CryptoClusters.ipynb 