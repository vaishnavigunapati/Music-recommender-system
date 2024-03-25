# Music-recommender-system
A **recommender** (or recommendation) **system** (or engine) is a filtering system which aim is to predict a rating or preference a user would give to an item, eg. a film, a product, a song, etc.

There are two main types of recommender systems:

- Content-based filters
- Collaborative filters

**Content-based methods** are computationally fast and interpretable. Moreover, they can be efficiently adapted to new items or users.  However, one of the biggest limitations of content-based recommendation systems is that the model only learns to recommend items of the same type that the user is already using or, in our case, listening to. Even though this could be helpful, the value of that recommendation is significantly less because it lacks the surprise component of discovering something completely new.

**Collaborative-based methods** work with an interaction matrix, also called rating matrix. The aim of this algorithm is to learn a function that can predict if a user will benefit from an item - meaning the user will likely buy, listen to, watch this item.

Among collaborative-based systems, we can encounter two types: **user-item**filtering and **item-item** filtering.

##
The aim of this project is to:

1. Generate a content-based music recommender system using a dataset of name, artist, and lyrics for 57650 songs in English obtained from Kaggle. The data has been acquired from LyricsFreak through scraping by the author.

2. Build a collaborative filtering music recommeder system using the Million Song Dataset; a freely-available collection of audio features and metadata for a million contemporary popular music tracks.

##
This repo is divided into the following two packages that contains the following files:

## I. Content-based recommendation system:

a. A jupyter notebook named content_based_music_recommender that contains the code and analysis for the recommedation system.
b. A CSV file named songdata containing the data for the songs used in the system.

## II. Collaborative recommendation system:

a. A jupyter notebook named collaborative_music_recommender that contains the code and analysis for the recommedation system.
b. A CSV file named songs containing the data for the songs used in the system.

Recommender has two filters:
## 1. Content-based filter
Recommendations done using content-based recommenders can be seen as a user-specific classification problem. This classifier learns the user's likes and dislikes from the features of the song.

The most straightforward approach is **keyword matching.**

In a few words, the idea behind is to extract meaningful keywords present in a song description a user likes, search for the keywords in other song descriptions to estimate similarities among them, and based on that, recommend those songs to the user.

How is this performed?

In our case, because we are working with text and words, **Term Frequency-Inverse Document Frequency (TF-IDF)** can be used for this matching process.
## 2. Collaborative filters
Collaborative Filters work with an interaction matrix, also called rating matrix. The aim of this algorithm is to learn a function that can predict if a user will benefit from an item - meaning the user will likely buy, listen to, watch this item.

Among collaborative-based systems, we can encounter two types: **user-item**filtering and **item-item** filtering.

What algorithms do collaborative filters use to recommend new songs? There are several machine learning algorithms that can be used in the case of collaborative filtering. Among them, we can mention nearest-neighbor, clustering, and matrix factorization.
1. K Nearest-neighbor
2. Clustering
3. Matrix Factorization

## 1. K Nearest-Neighbor
K-Nearest Neighbors (KNN) is a supervised machine learning algorithm used for classification and regression tasks. The basic idea behind KNN is to predict the class or value of a data point based on the majority class or average of its k nearest neighbors in the feature space. In the case of classification, the algorithm assigns the class that is most common among the k nearest neighbors. For regression, it calculates the average or weighted average of the target values of the k nearest neighbors. The choice of the parameter k influences the model's performance, as a smaller k value can lead to a more sensitive model, while a larger k value may result in a smoother decision boundary or regression curve. KNN is a simple and intuitive algorithm, but its computational complexity can be a limitation for large datasets.

K-Nearest Neighbors (kNN) is considered the standard method when it comes to both user-based and item-based collaborative filtering approaches.

## 2. Clustering
Clustering is a technique in unsupervised machine learning that involves grouping similar data points together based on certain criteria or features. The objective is to identify inherent patterns, structures, or relationships within the data without predefined labels. The goal of clustering algorithms is to partition the dataset into subsets, or clusters, where data points within the same cluster are more similar to each other than to those in other clusters.

There are various clustering algorithms, each with its own approach and strengths. Common methods include K-Means clustering, hierarchical clustering, and DBSCAN (Density-Based Spatial Clustering of Applications with Noise). K-Means, for instance, assigns data points to clusters by minimizing the sum of squared distances between points and their cluster centroids. Hierarchical clustering builds a tree-like structure of clusters, allowing for a more detailed exploration of the data hierarchy. DBSCAN, on the other hand, identifies clusters based on the density of data points in the feature space.

Clustering finds applications in diverse fields such as customer segmentation, image segmentation, anomaly detection, and pattern recognition. It is a valuable tool for gaining insights into the inherent structures of complex datasets, enabling better understanding and decision-making in various domains.

## 3. Matrix factorization
Matrix factorization is a mathematical technique commonly used in machine learning and data analysis, particularly in collaborative filtering and recommendation systems. The primary goal of matrix factorization is to decompose a given matrix into the product of two or more matrices, often with a lower rank, that approximates the original matrix. This decomposition helps reveal latent features or hidden patterns within the data.

In the context of recommendation systems, matrix factorization is frequently employed to model user-item interactions. The user-item matrix, where rows represent users, columns represent items, and the entries denote interactions or ratings, can be factorized into two matrices—one representing users and the other items. The multiplication of these matrices reconstructs the original matrix, capturing the underlying patterns in user preferences and item characteristics.

Matrix factorization has proven effective in dealing with sparse datasets, where not all users have interacted with all items. By capturing latent factors, it can predict missing values in the matrix, suggesting personalized recommendations for users. Singular Value Decomposition (SVD) is a classical matrix factorization method, and variations like Alternating Least Squares (ALS) and stochastic gradient descent are commonly used in collaborative filtering applications. Matrix factorization finds applications beyond recommendation systems, including image processing, signal processing, and dimensionality reduction in data analysis



