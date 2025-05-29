# Index
- Introduction to Recommendation System
- Exploratory Data Analysis(EDA)
- Content based filtering
- Collaborative Filtering
    - Memory based collaborative filtering
        - User-Item Filtering
        - Item-Item Filtering
    - Model based collaborative filtering
        - Single Value Decomposition(SVD)
        - SVD++
- Evaluating Collaborative Filtering using SVD
- Hybrid Model

# Introduction to Recommendation System
![image](https://github.com/user-attachments/assets/812bc649-1aef-4bd0-a0bf-485df532b03f)

### A recommendation system is any system that automatically suggests content, products or serivces which should interest customers based on their preferences.
![image](https://github.com/user-attachments/assets/08bb4e43-db0e-434f-8a3a-4d1b4fc3e10c)

## Why recommendation system is useful for orgnization?

#### - Help to increase the site’s page views, dwell time, click-through rate, and retention
#### - Help generate more advertising revenue
#### - Increase upselling and crossselling
![image](https://github.com/user-attachments/assets/dbb32145-49b0-4e18-817a-1d4102616c1a)
![image](https://github.com/user-attachments/assets/0ce3e8a1-3e60-414c-b4c5-5d6a6dea086b)

## How we build Recommendation Engine ?

![image](https://github.com/user-attachments/assets/d9492156-bb34-462e-ba4e-562764cceac8)

# Movie recommendation system
Recommender systems are one of the most successful and widespread application of machine learning technologies in business.
You can find large scale recommender systems in retail, video on demand, or music streaming.
- ***Examples of recommendation systems are:***
    1. Offering news articles to on-line newspaper readers, based on a prediction
of reader interests.
    2. Offering customers of an on-line retailer suggestions about what they
might like to buy, based on their past history of purchases and/or product
searches.
    3. Recommending movies to user based on there previous watch
 
# Content based filtering

- Content based system suggests you what you like based on what you liked in past.
- Recommendation of items are based on : user's previous purcheses, reviews and likes
- Combine: Item description and User profile description
- Generate similarity score
- Recommend the items based on similarity score

![image](https://github.com/user-attachments/assets/bcceb39a-60c5-4c98-ba27-112c439f110b)

The concepts of Term Frequency (TF) and Inverse Document Frequency (IDF) are used in information retrieval systems and also content based filtering mechanisms (such as a content based recommender). They are used to determine the relative importance of a document / article / news item / movie etc.

### Term Frequency (TF) and Inverse Document Frequency (IDF)
TF is simply the frequency of a word in a document. IDF is the inverse of the document frequency among the whole corpus of documents. TF-IDF is used mainly because of two reasons: Suppose we search for “the rise of analytics” on Google. It is certain that “the” will occur more frequently than “analytics” but the relative importance of analytics is higher than the search query point of view. In such cases, TF-IDF weighting negates the effect of high frequency words in determining the importance of an item (document).

We will consider genres as an important parameter to recommend user the movie he watches based on generes of movie user has already watched.
![image](https://github.com/user-attachments/assets/5d4edfff-ad8c-465c-8be9-bf42199b4856)


# Collaborative Filtering
Types of collaborative filtering techniques
* Memory based 
 - User-Item Filtering
 - Item-Item Filtering
* Model based 
 - Matrix Factorization
 - Clustering
 - Deep Learning
![image](https://github.com/user-attachments/assets/a99a185b-4304-4f4a-917f-ebae6048b88e)


## Memory Based Approach
![image](https://github.com/user-attachments/assets/32fa0181-ec07-4dad-856a-e7df589aecd6)

In either scenario, we builds a similarity matrix. For user-user collaborative filtering, the user-similarity matrix will consist of some distance metrics that measure the similarity between any two pairs of users. Likewise, the item-similarity matrix will measure the similarity between any two pairs of items.

There are 3 distance similarity metrics that are usually used in collaborative filtering:

- **Jaccard Similarity**
- **Cosine Similarity** 
- **Pearson Similarity** 
## Item-Item Filtering
Item-item collaborative filtering, or item-based, or item-to-item, is a form of collaborative filtering for recommender systems based on the similarity between items calculated using people's ratings of those items.


Item-item collaborative filtering was invented and used by Amazon.com
![image](https://github.com/user-attachments/assets/fd562ff9-6e8e-47cd-8b90-892b59829cf7)
ITEM-ITEM collaborative filtering look for items that are similar to the articles that user has already rated and recommend most similar articles. But what does that mean when we say item-item similarity? In this case we don’t mean whether two items are the same by attribute like Fountain pen and pilot pen are similar because both are pen. Instead, what similarity means is how people treat two items the same in terms of like and dislike.

It is quite similar to previous algorithm, but instead of finding user’s look-alike, we try finding movie’s look-alike. Once we have movie’s look-alike matrix, we can easily recommend alike movies to user who have rated any movie from the dataset. This algorithm is far less resource consuming than user-user collaborative filtering. Hence, for a new user, the algorithm takes far lesser time than user-user collaborate as we don’t need all similarity scores between users. And with fixed number of movies, movie-movie look alike matrix is fixed over time.

## User-Item Filtering
The underlying assumption of the collaborative filtering approach is that if a person A has the same opinion as a person B on an issue, A is more likely to have B's opinion on a different issue than that of a randomly chosen person.
![image](https://github.com/user-attachments/assets/a9b52bc6-6e21-47a3-ad3c-8199d08f2c3c)

Here we find look alike users based on similarity and recommend movies which first user’s look-alike has chosen in past. This algorithm is very effective but takes a lot of time and resources. It requires to compute every user pair information which takes time. Therefore, for big base platforms, this algorithm is hard to implement without a very strong parallelizable system.

## Pros and Cons of two methods

Challenges with User similarity
- The challenge with calculating user similarity is the user need to have some prior purchases and should have rated them.
- This recommendation technique does not work for new users.
- The system need to wait until the user make some purchases and rates them. Only then similar users can be found and recommendations can be made. This is called cold start problem.

# Single Value Decomposition

Singular value decomposition is a method of decomposing a matrix into three other matrices:

![image](https://github.com/user-attachments/assets/919ea132-8a80-435f-9275-41ba915502f4)



