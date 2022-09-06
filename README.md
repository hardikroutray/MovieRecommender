I realized that I have never actively rated any movie on Netflix or Amazon Prime. Maybe, that's the reason why the recommendations are not upto the mark ? Using only the watched movies and my profile data, the recommender system probably only suggests similar movies based on some norm. 

Instead of actively rating the movies on netflix and thanks to Andrew Ng's tutorial on recommender systems, I built a recommender system to suggest me movies based on my tastes. The two main approaches are briefly described below and can be looked up in the notebooks.

## Collaborative Filtering

As the name suggests, the movie rating predictions for a user is a result of collaborative data of all the users. No explicit movie features or user features are required. Those feature vectors will be obtained using only the ratings data. Based on the ratings of the user, they are recommended movies liked by users with similar ratings.

## Content Filtering

In contrast to collaborative filtering, we have extra information about the users and the movies like the genres and average rating etc. Using this extra information and the ratings, we also obtain user feature vectors and movie feature vectors. Two neural networks (one for user and movie each) are simultaneously trained. For faster recommendations, the movie feature vectors are stored along with the distances b/w them after training. This allows the recommender system to instantly suggest movies similar to the movies already liked by the user. Later, the trained user neural network is used to evaluate the user feature vector and subsequently the predicted ratings. 

