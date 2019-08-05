# What is it ? Global overview
This project is only for educational purposes. I did it while I was following the `Udacity DataScience nanodegree`.  
In this project, we are given real-life data provided by `Bertelsmann` partners `AZ Direct` and `Arvato Finance Solution`.  
**As those data are confidential they are not provided within this repository.**  
The data concerns a company that performs mail-order sales in Germany. Their main question of interest is to identify facets of the population that are most likely 
to be purchasers of their products for a mailout campaign. 
Our job is to use unsupervised learning techniques to organize the general population into clusters, then use those clusters to see which of them comprise the main
user base for the company.
But, as there are many features, prior to applying the machine learning methods, we need to assess and clean the data in order to convert the data into a usable form
and then apply principal Component Analysis (PCA) to find the vectors of maximal variability.

# 3 steps to go
## Step 1: Preprocessing
Explore and understand the data that we are working with. Here we are working with the general demographics data.
As part of our investigation of dataset properties, we must attend to a few key points:
* How are missing or unknown values encoded in the data ?
* Are there certain features (columns) that should be removed from the analysis because of missing data ?
* Are there certain data points (rows) that should be treated separately from the rest ?

Considering the level of measurement for each feature in the dataset (e.g. categorical, ordinal, numeric):
* What assumptions must be made in order to use each feature in the final analysis ?
* Are there features that need to be re-encoded before they can be used ?
* Are there additional features that can be dropped at this stage?

## Step 2: Feature Transformation
Once data is clean, we use dimensionality reduction techniques to identify relationships between variables in the dataset, resulting in the creation of a new set
of variables that account for those correlations.  
The first technique to perform on data is feature scaling and then apply principal Component Analysis (PCA) to find the vectors of maximal variability.
* How much variability in the data does each principal component capture ?
* Can we interpret associations between original features based on the weights given on the strongest components ?
* How many components will we keep as part of the dimensionality reduction process ?
For that we will use the sklearn library to create objects that implement feature scaling and PCA dimensionality reduction decisions.

## Step 3: Clustering
Finally, on our transformed data, we can apply clustering techniques to identify groups in the general demographic data. 
And then we are able to apply the same clustering model to the customers dataset to see how market segments differ between the general population and the mail-order
sales company.
We will use the K-Means method to cluster the demographic data into groups.