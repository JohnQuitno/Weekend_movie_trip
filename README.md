Weekend Movie Trip
==============================

Movie Clustering users

Project Organization
------------


    ├── data
    │   └── raw   
    │        │── Movie Data                     
    │
    ├── notebooks          
    │   └── src.ipynb               


Data
----
I'm looking at a data set that contains roughly 100000 reviews among 1000 people rating 1600 movies.
There is quite a lot of information here associated with each of these rows. The user information
contains things like location, age and profession data. The Movies data gives us the genre of each
movie. We also see timestamps on the rating data here.

Feature Engineering
-------------------
There are a lot of things that we could be doing here to group these users. The end goal is to be 
able to recommend movies to people that they will watch and enjoy. You could imagine that we can look 
at profession, movie genre, age and a bunch of these other features that might be able to predict 
what movies people like. I kept it simple and just used the watch history grouped by genre of the users. 
I counted the number of movies each has rated in the respective genres, and then created clusters of users
based on that genre data. This gives clusters of people who all enjoy watching the same type of movie. 

Classification Algorithms
-------------------------

I used both Kmeans and Meanshift here. Kmeans is the most simple of the clustering algorithms. The 
algorithm needs to be given a number of clusters to run. This is hard to reason about. I wasn't 
really sure what the best number of groups to be broken up into was so I ended up running Kmeans with
10 groups because that was a number that was discussed as reasonable in class. The second algorithm 
that I used was meanshift. 