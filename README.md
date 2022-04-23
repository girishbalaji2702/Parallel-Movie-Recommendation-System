# Parallel-Movie-Recommendation-System

Our proposed system is to implement a movie recommendation system using collaborative 
filtering approach. These recommendations should be based on a user’s previous watch history 
as well as movies that similar users have watched and also the ratings. Therefore, computing 
how similar two users are is an essential part of the recommendation process. Good 
recommendations benefit both customers, who are suggested to watch movies that are better 
suited to their liking and are able to save time, as they are able to host a greater number of 
movies, successfully market new movies, and obtain customer loyalty as watching new movies 
increases the quality of recommended movies.

Thus the proposed ALS system will overcome these problems using the Matrix factorization 
method. This increases the scalability as well as the speed of the recommender systems. 

From the above discussion we can see that the existing system is not really accurate and also 
has many disadvantages. On top of these it is slow compared to the ALS approach. Thus, in 
order to parallelize the KNN based approach we introduce another method using ALS based 
on which the system will be parallelized. 

To run the knn.py  :-
ex. python src/knn.py --movie_name "Iron Man" --top_n 10

Torun als.py  :-
ex. spark-submit --master local[4] --driver-memory 4g 
             --executor-memory 8g src/als.py 
             --movie_name "Iron Man" --top_n 10
