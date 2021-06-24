# Recommendation-System-using-truncated-SVD
### Recommendation System (like Netflix) using truncated SVD with SGD Classifier and SURPRISE Library

<p>
Platforms like Netflix and Hotstar help customers find the movies they love and will like and then recommend. They develope dedicated world-class movie recommendation system like CinematchSM from Netflix. Its job is to predict whether someone will enjoy a movie based on how much they liked or disliked other movies. Netflix use those predictions to make personal movie recommendations based on each customer’s unique tastes.
</p>

Data is available heer: https://www.kaggle.com/netflix-inc/netflix-prize-data

Goal:
1. Predict the rating that a user would give to a movie that he ahs not yet rated.
2. Minimize the difference between predicted and actual rating (RMSE and MAPE)


For a given movie and user we need to predict the rating would be given by him/her to the movie. 
The given problem is a Recommendation problem. It can also seen as a Regression problem.

1) The data is downloaded in form of text file with userid, movieid, ratings and the timestample.
2) The preprocessing is done and feature engineering to see which feature is important. 
3) Then the preprocessing involves stroing data in form of tuple (userid, movieid, rating) after arranging them with timestamps as it has temporal component. 
4) The data will be of this format, each data point is represented as a triplet of user_id, movie_id and rating 
<table>
<tr><th>user_id</th><th>movie_id</th><th>rating</th></tr>
<tr><td>77</td><td>236</td><td>3</td></tr>
<tr><td>471</td><td>208</td><td>5</td></tr>
<tr><td>641</td><td>401</td><td>4</td></tr>
<tr><td>31</td><td>298</td><td>4</td></tr>
<tr><td>58</td><td>504</td><td>5</td></tr>
<tr><td>235</td><td>727</td><td>5</td></tr>
</table>

5) Then we use matrix factorization i.e SVD and truncate them to get the feature with highest variance.
6) Then we use SURPRISE library : https://surprise.readthedocs.io/en/stable/index.html and different models from it. 
7) Surprise is an easy-to-use Python scikit for recommender systems.
8) Then we also use SGD Classifier to make predictions given userid and movieid. 
9) The metric used is MSE  and MAPE.


Important links:
https://surprise.readthedocs.io/en/stable/similarities.html#surprise.similarities.pearson_baseline
https://surprise.readthedocs.io/en/stable/knn_inspired.html#surprise.prediction_algorithms.knns.KNNBaseline
