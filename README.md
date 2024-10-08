# MSML-602 Group Project

Group members:
1.Karthik Ramanathan
2.Ali Fehmi Yıldız
3.Murugavel Suresh
4.Anagha Giridhar
5.Saanvi Joginipally

The project Dataset Location: https://grouplens.org/datasets/movielens/1m/
PROCESSING AND CLEANING STEPS

Handling Missing Values:
We will check for missing values in critical columns such as userId, movieId, and rating to ensure our dataset is complete and does not cause errors during analysis.

Removing Duplicates:
We will ensure no duplicate entries exist by identifying and removing repeated rows in the dataset. Each user-movie interaction should be unique for accurate recommendations.

Data Type Conversion:
We will convert the timestamp column into a readable DateTime format and ensure that userId, movieId, and rating are in the correct data types (integer for userId and movieId, and float for rating).

Handling Ratings Outliers:
We will validate that all ratings fall within the expected range (e.g., between 1 and 5). Any outliers or erroneous ratings will be removed or corrected.

Validating Data:
We will implement checks to ensure data validity. We will ensure that user information is applicable, such as a minimum age requirement (e.g., a user cannot be 1 year old to vote on a movie). Invalid data will be corrected or removed.

Dealing with Inconsistent Data:
We will check for any inconsistencies, such as multiple entries for the same movie under slightly different names or variations of the same genre (e.g., "Sci-Fi" and "Science Fiction"). These inconsistencies should be standardized.

Genre Processing:
Since some movies have multiple genres listed, we might want to break down or encode these genre lists using one-hot encoding or multi-label binarization for better modeling.

Filtering Out Inactive Users:
We will consider removing users who have rated only a very small number of movies, as they may not provide enough information to build a meaningful user profile. Setting a threshold (e.g., users with fewer than 5 ratings) can help in focusing on active users.

Movie Popularity Filtering:
Similar to filtering inactive users, we may also choose to remove movies that have very few ratings. Movies that have been rated by only a handful of users may not provide enough data for effective recommendations.

Handling Timestamp Granularity:
Depending on the goal of our analysis, we may need to adjust the granularity of the timestamp. For instance, we could group ratings by month or year, instead of the exact time of rating, to capture trends over time more effectively.

Handling User Demographic Data:
If demographic information (age, gender, occupation) is included in the dataset, we can also validate and clean these fields (e.g., removing unrealistic ages or ensuring occupation labels are consistent).

Creating Additional Features:
We can create new features such as the number of ratings per user, the average rating per user, or the average rating per movie to enrich the dataset for recommendation algorithms.

*** Project Part 2 ***

1. The features that we are going to use are as follows:
userId, movieId, title, genres

The predicted column will be:
rating

2. We will encode genre lists to accomadate the multiple genres per movie issue. Also creating a new feature, average rating of users will help improve the data and result in more accurate predictions 


3. The data isn't highly imbalanced but regardless to create a model with high efficacy and unbiased results we will be using methods like :
   1. Oversampling the movies that have received the least ratings
   2. Adding higher weights to the minority classes i.e, the movies with lower ratings

