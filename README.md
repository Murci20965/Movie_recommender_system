# Movie Recommendation System On MovieLens Datasets
### Project Overview
This project aims to develop a robust movie recommendation system using collaborative filtering techniques, specifically Singular Value Decomposition (SVD), on a dataset of movie ratings. The system leverages user preferences and behavior to provide personalized movie recommendations, enhancing the overall user experience and engagement.

### Recommender Systems Overview
A recommender system is a specialized information filtering system designed to predict a user's preference or rating for an item. These systems are widely used across various domains such as movies, music, news, social tags, and general products. They generate personalized lists of recommendations through different methodologies. Two of the most prominent methods are collaborative filtering and content-based filtering.

**ADD IMAGE HERE**

Recommender systems power many of the internet products we use daily. Platforms like YouTube, Netflix, Amazon, and Pinterest rely heavily on these systems to sift through millions of items and provide personalized suggestions to their users. The effectiveness of recommender systems in improving user satisfaction and engagement is well-documented, making them essential tools for modern internet businesses.

Types of recommender systems primarily in the Media and Entertainment industry:

- Collaborative Recommender system
- Content-based recommender system
- Knowledge based recommender system
- Hybrid recommender system
- Demographic based recommender system
- Utility based recommender system


A recommender system is a complex and multifaceted concept that revolves around providing users with personalized suggestions. Various algorithms are employed to construct these systems, and the choice of algorithm largely depends on the nature of the available data. In this project, I implemented a collaborative filtering approach using Singular Value Decomposition (SVD) to develop A movie recommendation system.

**Collaborative Filtering**
Collaborative filtering makes recommendations based on the preferences of similar users. This can be done using user-based or item-based methods. User-based collaborative filtering finds users who are similar to the target user and recommends items they liked. Item-based collaborative filtering finds items similar to those the user has liked in the past.

**Common Challenges**
Recommender systems face several challenges during development and deployment:

- **Cold Start Problem:** Difficulty in making recommendations for new users or items with no historical data.
- **Scalability:** Handling large datasets efficiently to provide timely recommendations.
- **Sparsity:** Dealing with the vast majority of possible user-item interactions being unrated or unobserved.
- **Diversity:** Ensuring the recommendations do not become too homogeneous, limiting user exposure to different items.
- **Privacy:** Balancing the use of personal data to make recommendations while protecting user privacy.

### Data Overview:
This dataset comprises millions of 5-star ratings provided by users of the MovieLens online movie recommendation service. The MovieLens dataset has been a staple for both industry and academic researchers to enhance the performance of recommendation systems based on explicit user feedback.

In this project, I utilize a specially curated version of the MovieLens dataset, enriched with additional data and resampled to ensure fair evaluation. The GroupLens research group at the Department of Computer Science and Engineering, University of Minnesota, maintains this dataset. Additional movie metadata was legally sourced from IMDB.

**Supplied Files:**
- **genome_scores.csv** - A score mapping the strength between movies and tag-related properties.
- **genome_tags.csv** - User-assigned tags for genome-related scores.
- **imdb_data.csv** - Additional movie metadata scraped from IMDB using the links.csv file.
- **links.csv** - Provides a mapping between a MovieLens ID and associated IMDB and TMDB IDs.
- **sample_submission.csv** - Sample of the submission format for the hackathon.
- **tags.csv** - User-assigned tags for the movies within the dataset.
- **test.csv** - The test split of the dataset containing user and movie IDs with no rating data.
- **train.csv** - The training split of the dataset containing user and movie IDs with associated rating data.

### Objectives
1. **Personalized Recommendations:** Provide users with movie suggestions based on their historical preferences and behavior.
2. **Enhanced User Experience:** Improve user satisfaction by offering relevant and tailored movie choices.
3. **Engagement:** Increase user engagement and interaction with the platform through targeted recommendations.
4. **Business Value:** Drive business growth and revenue by keeping users engaged and satisfied, leading to increased retention and loyalty.
   
### Methodology
The system employs collaborative filtering, specifically Singular Value Decomposition (SVD), to analyze user-item interactions and predict movie ratings. It utilizes historical user data and movie features to generate accurate recommendations.

### Key Features
1. **User Profiles:** Captures user preferences, ratings, and viewing history.
2. **Movie Database:** Contains information about movies, including titles, genres, and ratings.
3. **Recommendation Engine:** Uses SVD to generate personalized movie recommendations.
4. **Evaluation Metrics:** Measures system performance using RMSE (Root Mean Squared Error) and Bayesian average ratings.

### Recommender System Using SVD
#### Approach
In this project, I developed a movie recommendation system using the MovieLens dataset enriched with additional data from IMDB. My primary approach leveraged collaborative filtering using Singular Value Decomposition (SVD) to predict user ratings and recommend movies. Below, I detail my approach and the mathematical foundation of SVD used in the project.

**Data Processing**

**1. Data Cleaning:**

- Began by loading the datasets, which included ratings, movieIds, userIds, tiltes, and genres.
Missing values were handled appropriately to ensure a clean dataset for analysis.

**2. Data Integration:**

- Merged the train dataset with the movie dataset during EDA.

**3. Data Preparation:**

- Split the dataset into training and test sets to evaluate the performance of the recommender system.
  
**Collaborative Filtering with SVD**
**Collaborative filtering** predicts user preferences by analyzing the preferences of many users. The underlying assumption is that if users have agreed in the past, they will likely agree in the future.

**Singular Value Decomposition (SVD)** is a powerful matrix factorization technique used in collaborative filtering to decompose the user-item interaction matrix into lower-dimensional matrices.

**Mathematical Foundation of SVD**

Given a user-item rating matric ***R*** with *m* users and *n* items, SVD factorizes ***R*** into three matrices:

***R***≈***UΣV^T***

Where: 
- ***U*** is *m* × *k* orthogonal matrix, representing the user features.
- ***Σ*** is a *k* × *k* diagonal matrix, containing the singular values.
- ***V*** is an *n* × *k* orthogonal matrix, representing the item features.
- ***k*** is the number of latent factors, much smaller than 𝑚 and 𝑛.

**Steps to implememt SVD**

  **1. Matrix Factorization:**
  -
  -

  **2. Dimensionality Reduction:**
  -
  -

  **3. Prediction:**
  -
  -

  **4. Evaluation:**

  - Evaluated the model using metrics such as Root Mean Squared Error (RMSE) on the test set.
  - This helped assess the accuracy and effectiveness of the recommendation system.
    
**Practical Implementation**

  **1. Libraries Used:**
  - Utilized Python libraries such as **'pandas'**, **'numpy'**, and **'scikit-learn'** for data processing and model building.
  - The **'Surprise'** library was used for implementing the SVD algorithm Application.

  **2. Algorithm Application:**
  - The training data was fed into the SVD algorithm to learn the user and item latent factors.
  - tuned the hyperparameters (such as the number of factors, learning rate, and regularization) to optimize the model's performance.

  **3. Genereating Recommendations**
  - Once trained, the model was used to predict ratings for unseen user-item pairs.
  - Based on these predictions, we generated a list of top recommended movies for 4 chosen users.

**Key Achievements**
- Successfully implemented SVD to factorize the user-item interaction matrix.
- Achieved a low RMSE score, indicating accurate rating predictions.
- Developed a recommendation system that can efficiently handle large-scale data.

By leveraging the power of SVD in collaborative filtering, I was able to create an effective movie recommendation system that provides personalized suggestions based on user preferences.

### Insights and Recommendations
- **Personalized Experience:** Users receive movie recommendations tailored to their tastes and preferences, leading to higher user satisfaction and engagement.
- **Increased User Interaction:** The system encourages users to explore new movies and genres, boosting user interaction and platform usage.
- **Improved Retention:** By offering relevant content, the system increases user retention and loyalty, reducing churn rates.
- **Business Growth:** Satisfied users are more likely to continue using the platform and recommend it to others, contributing to business growth and success.

### Code Explanation
1. **Data Preprocessing:** The notebook (movie-recommender-system.ipynb) begins with loading and exploring datasets (train.csv, test.csv, movies.csv) to understand the data structure and identify any missing values.
2. **Collaborative Filtering:** Utilizes Singular Value Decomposition (SVD) to build a recommendation engine that predicts movie ratings based on user-item interactions.
3. **Grid Search for Parameter Tuning:** Employs grid search with cross-validation to find the best parameters for the SVD model, optimizing performance metrics such as RMSE.
4. **Model Training and Evaluation:** Trains the SVD model using the best parameters and evaluates its performance on a validation set. It also predicts ratings for the test set to generate recommendations.
5. **Submission Generation:** Generates a CSV file (submission.csv) containing user-movie rating predictions for submission or further analysis.

### Importance in Today's World
In today's digital landscape, personalized recommendation systems play a vital role in enhancing user experience across various platforms. With the abundance of content available, users seek personalized and relevant recommendations to streamline their decision-making process. A robust recommendation system not only improves user satisfaction but also drives business growth by fostering user engagement and loyalty.

### Business Benefits
- **Enhanced User Engagement:** Users spend more time on the platform, exploring recommended content and interacting with the system.
- **Increased Revenue:** Engaged and satisfied users are more likely to make repeat purchases or subscriptions, contributing to revenue growth.
- **Competitive Advantage:** A sophisticated recommendation system sets the platform apart from competitors, attracting and retaining users.
- **Data Insights:** The system generates valuable insights into user preferences, behavior, and trends, informing business strategies and content decisions.

### Conclusion
The movie recommendation system is a strategic asset that enhances user experience, drives user engagement, and contributes to business success. By leveraging collaborative filtering techniques and personalized recommendations, the system delivers value to both users and stakeholders, positioning the platform for growth and innovation.
