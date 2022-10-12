
# Movie Recommender System

Content Based Recommender System recommends movies similar to the movie selected by an user and recommends movies based on cosine similarity with the other movies.

Built a web application using Streamlit and deployed on Heroku-app.
Check out the application- https://mrs-chandu.herokuapp.com/



![alt text](https://img.shields.io/badge/Python-3.9-green) 
![alt text](https://img.shields.io/badge/Framework-Streamlit-red) 
![alt text](https://img.shields.io/badge/API-TMDB-yellowgreen)


## Overview

A recommender system that recommends movies to the user based on the cosine similarity among the movies. The main parameters that are considered for the recommendations are the genre, director, and top 3 casts.

### Data Preprocessing

At first we have to make sure the data is cleaned for further analysis. 
* Converted genre, keywords columns and cast as a list of strings, and for the cast column I have selected the top 3 casts for each movie.
* For the crew column I have selected the name of the Director.
* Omitted the spaces between the names of the cast and crew in order to get rid of the confusion.
* Combined all five columns- overview, genres, keywords, cast and crew into a single columns named tags.
* Converted all the upper cases to lower cases.

### Text Vectorization

Text Vectorization is a method to represent words, sentances or even larger units of text as vectors.
Types of text vectorization
* Bag of Words
* TF IDF
* Word to Vector
I have used Bag of Words to tokenize the input sequences. I have used CountVectorizer for this.

I calculated cosine similarity among each vectors and stored them as a matrix similarity.
#### Similarity Score:
How does it decide which item is most similar to the item user likes? Here come the similarity scores. It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.
#### Cosine Similarity
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.

![](https://user-images.githubusercontent.com/36665975/70401457-a7530680-1a55-11ea-9158-97d4e8515ca4.png)
