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

