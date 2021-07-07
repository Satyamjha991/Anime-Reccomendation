# Anime Reccomendation System
With the ability of machine learning, we explore the dataset to create a recommendation system with the ability to help
someone to find what to watch next.

## Introduction:


### Dataset 
#### 2.1 Context
Every streaming content has its own viewers and each content has it’s rating. Viewers leave some good ratings for the
content if they like it. But where does it apply? Viewers can spend hours scrolling through hundreds, sometimes
thousands of anime's, never finding any content they like. Businesses need to provide suggestions based on their likes
and needs in order to create a better streaming environment that boosts revenue and increases the time spent on a
website.
#### 2.2 Objectives:
Implement Collaborative Filtering and content based filtering for recommendation systems.
#### 2.3 Problem Statement
Using an anime dataset, to create a recommendation system based on two famous algorithms of content based and collaborative filtering recommendation systems. These algorithms are implemented from scratch with other variations to overcome limitations of each other.

## Materials and Methods 
### 3.1 Dataset description
* For this project I have downloaded anime and user ratings from: https://github.com/Hernan4444/MyAnimeList-Database. 
* This dataset contains information about 17,562 anime and the preference from 57,633,278 different users.
*  Ratings given by users to the anime that they have watched completely.
* Information about the anime like genre, stats, studio, etc.
* Synopsis of the anime as per myanimelist.com
* Ratings are in range from 1 - 10 with global avg rating of 7.80

### 3.2 Technologies:
Python: For writing basic algorithms using data structures of python.
Pandas: Pandas dataframe for querying over the data tables.
Skit-learn:To implement TF_IDF, Similarities and other metric operations 
Matplotlib: For visualizing the data.

### 3.3 Algorithms
#### 3.3.1 Content Based Recommendation System
This algorithm recommends products which are similar to the ones that a user has liked in the past. The content of each
item is represented as a set of descriptors or terms, typically the words that occur in a document.A content based recommender
works with data that the user provides, either explicitly (rating) or implicitly (clicking on a link). Based on that data, a user profile is
generated, which is then used to make suggestions to the user. As the user provides more inputs or takes actions on the
recommendations, the engine becomes more and more accurate
##### Here, there are various approaches to solve this problem and I have applied them keeping in mind their usage in theindustry.
They are broadly based on 2 category:
1) User Based: Takes user_id to get recommendation
2) Item Based: Give recommendation based on the serch
We use cosine similarity to find the relation
Cosine similarity metric measures the cosine of the angle between two n-dimensional vectors projected in a
multi-dimensional space. The Cosine similarity of two documents will range from 0 to 1.

#### 3.3.2 Collaborative Filtering Recommender System
Collaborative filtering is a technique that can filter out items that a user might like on the basis of reactions by similar users. It works by
searching a large group of people and finding a smaller set of users with tastes similar to a particular user.
1) User-User collaborative filtering- This algorithm first finds the similarity score between users. Based on this
similarity score, it then picks out the most similar users and recommends products which these similar users have liked
or bought previously.
2) Item-Item collaborative filtering: In this algorithm, we compute the similarity between each pair of items. So in our
case we will find the similarity between each movie pair and based on that, we will recommend similar movies which
are liked by the users in the past.

## Discussion:
A major drawback of content based filtering algorithm is that it is limited to recommending items that are of the same type. It will never
recommend products which the user has not bought or liked in the past. So if a user has watched or liked only action movies in
the past, the system will recommend only action movies. It’s a very narrow way of building an engine.
To improve on this type of system, we need an algorithm that can recommend items not just based on the content, but the
behavior of users as well.
In practice, many commercial recommender systems are based on large datasets. As a result, the user-item matrix used
for collaborative filtering could be extremely large and sparse, which brings about challenges in the performance of the
recommendation.One typical problem caused by the data sparsity is the cold start problem. As collaborative filtering
methods recommend items based on users' past preferences, new users will need to rate a sufficient number of items to
enable the system to capture their preferences accurately and thus provides reliable recommendations.
Similarly, new items also have the same problem. When new items are added to the system, they need to be rated by a
substantial number of users before they could be recommended to users who have similar tastes to the ones who
rated them. The new item problem does not affect content-based recommendations, because the recommendation of
an item is based on its discrete set of descriptive qualities rather than its ratings.

#### Future Possible Ideas:
Creating a hybrid recommendation system that that combines content-based filtering and collaborative filtering could
potentially take advantage from both the representation of the content as well as the similarities among users and
negates the limitations.
Testing the model with the appropriate algorithm.

## References:
https://www.analyticsvidhya.com/blog/2015/08/beginners-guide-learn-content-based-recommender-systems/
https://github.com/Hernan4444/MyAnimeList-Database
https://www.analyticssteps.com/blogs/what-are-recommendation-systems-machine-learning
https://builtin.com/data-science/recommender-systems



