<p align="center">
  <img width="600" height="300" src="https://github.com/a-pradono/FIFA-clusters/blob/main/Images/fifa-header.jpg">
</p>

## Table of Contents

- [I. Introduction](#i-introduction)
- [II. Data and Methodology](#ii-data-and-methodology)
- [III. Results](#iii-results)
- [IV. Conclusions](#iv-conclusions)

## I. Introduction
One of my favorite video games on PlayStation is FIFA and I have played this game for about 11 years with some friends during our free time. FIFA is also known as one of the best-selling video game franchises under the EA Sports label. You can play with available national and club teams against CPU or your friends on your console. As someone who has grown up playing FIFA, it came to my realization that I should apply my data analytics skills to my favorite soccer video game. The objective of this project was to divide various players into several number of groups with similar skills as possible by using clustering algorithms.

## II. Data and Methodology
This data was obtained from FIFA 21 complete player dataset, posted by Stefano Leone, consisting of +18K rows and +100 columns, and can be found on [www.kaggle.com](https://www.kaggle.com/stefanoleone992/fifa-21-complete-player-dataset). 

<p align="center">
  <img width="900" height="200" src="https://github.com/a-pradono/FIFA-clusters/blob/main/Images/workflow.png">
</p>

The workflow above demonstrates how I performed clustering analysis. Starting with the input data, I have performed data cleaning which resulted in creating a new data frame that includes only numeric values with overall players above 85. Furthermore, normalization has been performed before I applied principal component analysis (PCA) to reduce dimensionality in the data frame. Thus, the data was ready to create K-means clustering algorithms with the optimal number of clusters based on the elbow method. Finally, the scatter plot illustrates how players have been set into a number of groups. 

## III. Results
Just out of curiosity, these plots below show the distribution of player's physical characteristics and income who have overall above 85. One of the boxplots has an outlier in the player wage distribution plot with a wage of over 500000 euro per week.

<p align="center">
  <img width="900" height="600" src="https://github.com/a-pradono/FIFA-clusters/blob/main/Images/plot001.png">
</p>

The elbow method was constructed to find the optimize a number of clusters by fitting the model with a range of values for K in K-means algorithm as shown below. This plot was using a line plot between values of K and inertia or sum of squared error (SSE). Inertia is calculated by measuring the distance between each data point and its centroid, squaring the distance, and summing these squares across one cluster. On top of that, inertia measures how well a dataset was clustered by K-means = 4 based on where the decrease in inertia begins to slow.

<p align="center">
  <img width="500" height="300" src="https://github.com/a-pradono/FIFA-clusters/blob/main/Images/plot002.png">
</p>

The scatter plot has been developed to visualize the results of K-means clustering. There are four clusters including cluster 0, cluster 1, cluster 2, and cluster 3. If you are familiar with soccer, you will notice that the plot below illustrates how player skills are clustered by their positions. Cluster 0 can be identified as a striker, cluster 1 as a goalkeeper, cluster 2 as a defender, and cluster 3 as a midfielder. Although there is some little mixing between midfielder and defender, the cluster results did a pretty good job generally. Some players in these clusters: cluster 0 L. Messi and Cristiano Ronaldo; cluster 1 De Gea and T. Courtois; cluster 2 M. Hummels and G. Chiellini; cluster 3 P. Pogba and T. Kroos.

<p align="center">
  <img width="800" height="600" src="https://github.com/a-pradono/FIFA-clusters/blob/main/Images/plot003.png">
</p>

## IV. Conclusions
The objective of this project was to create a number of groups of FIFA players based on similar skills by implementing K-means clustering algorithms. The conclusions made from this project are:
  * Within minutes, FIFA players have been grouped into several positions based on their similar skills.
  * Some of the positions seemed a bit blurred. For example, defender and midfielder.
  * Overall, the clustering methods are easy to implement, relatively fast, and efficient.
