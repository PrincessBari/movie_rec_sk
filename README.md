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
