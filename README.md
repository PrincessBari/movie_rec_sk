# movie_rec_sk

# OBJECTIVE
I wanted to build a collaborative filtering recommendation system using MovieLens data. I downloaded a ratings dataset and a movies dataset from https://grouplens.org/datasets/movielens/. Out of the various datasets available, I chose the one labeled "recommended for education and development" which, according to the source website, has approximately 100k ratings and 9k movies by 600 users.

# Part 1
In the first part, I built a user-item CF recommendation system using the movies and ratings datasets. We transform our data into a user-item matrix with rows representing users and columns representing items. And we build our K-Nearest Neighbors model.

# Part 2
In the second part, I built a content-based item-item recommendation system using just the movies dataset. This was interesting to me because collaborative filtering suffers notoriously from something called the cold-start problem in which new users or items with no ratings/interactions get excluded by the recommender system. So using content-based filtering, recommendations are generated based on user and item features. 

# Reflection
In part one, the way the recommender system was built, you can only input the movie_id number instead of the movie name. For example, movie_id number 1 stood for "Toy Story (1995)". In the future, I would want to tweak this to figure out how to either add a step, such as in part where you enter a movie title, and it spits out the movie index number for you. I was unable to transfer and tweak the code from part 2 into part 2 because the matrices were built different for each part. 

For part two, in the future I would want to tweak how the fuzzy wuzzy string input function works. As of now, any typing error you make must result in a word that is still very, very similar to the existing movie title. If it's too different, it will misidentify the movie you intended to input. Another issue with this is that you could input a correctly spelled movie title that doesn't exist in the system, and that may also misidentify the movie as something else. For example, I inputted the Afrofuturist film "Space is the Place" which doesn't exist in the system, and it returned recommendations for "Father of the Bride II (1995)".

==============
# UPDATED FINAL PROJECT PROPOSAL

# Introduction 
   My final project proposal was to build a recommendation model for world music vinyls, but after having some issues finding data, I ended up using movie data, specifically MovieLens datasets.
 
# A description of the data you intend to use
   I had initially planned to use the full roster of albums released by Monitor Records and the Explorer Series imprint of Nonesuch Records of which between the two there are a total of about 325 albums combined. I had specifically started with these two labels because - of the world music albums I own and love - my favorites seem to come from these two. 
   Again, because I had to change my project, I ended up using a ratings dataset and a movies dataset from https://grouplens.org/datasets/movielens/. Out of the various datasets available, I chose the one labeled "recommended for education and development" which, according to the source website, has approximately 100k ratings and 9k movies by 600 users.
 
# Machine learning task
   The machine learning task I carried out were user-item and item-item collaborative filtering via the KNN algorithm. 
 
# A tentative and brief survey of existing work on the topic
	I’ve gone over a few papers so far associated with this topic. In the piece “Various Implementations of Collaborative Filtering,” the programmer explains that “The most basic models for recommendations systems are collaborative filtering models which are based on the assumption that people like things similar to other things they like, and things that are liked by other people with similar tastes.”  
   In another paper, “Attribute-Aware Recommender System Based on Collaborative Filtering: Survey and Classification,” the authors go over how the attribute-aware recommender system model based on collaborative filtering is more effective than the classical matrix factorization collaborative filtering method that uses only ratings – which apparently suffers a drawback by being unable to exploit other accessible information, such as the attributes of users/items/ratings. 
   In another paper, “Exploration in Interactive Music Recommendation: A Reinforcement Learning Approach,” I was introduced to the cold-start problem - a notorious problem that collaborative filtering suffers from - in which the collaborative filtering method cannot recommend songs to new users whose preferences are unknown (the new-user problem) or recommend new songs to users (the new-song problem). 
   As a result, in contrast, some data scientists might turn to content-based methods, which recommend songs with audio content - which refers to acoustic features, such as timbre and rhythm - similar to the user’s preferred songs. However, content-based systems solve the new-song problem but not the new-user problem. Therefore, context-based music recommender systems have become increasingly popular. They recommend songs to match various aspects of the user context - such as activities, locations, environment, mood, physiological states, etc - or text context. 
   In the paper “Recommender System Using K-Nearest Neighbors and Singular Value Decomposition Algorithms: A Hybrid Approach,” it is discussed how there are two types of collaborative filtering approaches: memory-based collaborative filtering and model-based collaborative filtering.
   Memory-based collaborative filtering can be divided into two main sections: user-item filtering and item-item filtering. In user-item filtering, a particular user is chosen, and similar users are found based on the similarity of the ratings, and then items are recommended that similar users also liked. In item-item filtering, an item is chosen, and then those users are found who liked that item, and then other items are found that those users or similar users also liked.
   In model-based collaborative filtering, collaborative filtering models are developed using various machine learning algorithms - clustering-based, matrix factorization-based, and deep learning based - to predict user ratings of unrated items. Out of the three approaches, the deep learning-based algorithm has the best accuracy overall.
 
# A discussion of the significance of your topic
   Recommendation systems are so very popular now that I felt this could be a good opportunity to learn how they work and to apply it to something I’m very excited about.  
