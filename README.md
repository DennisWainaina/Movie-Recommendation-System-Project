![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/10fad608-693e-4202-b7f5-fdff0fd58569)

## PHASE 4 FINAL PROJECT

## INTRODUCTION
**Welcome to My Recommendation System Project Repository**

This repository houses the code and documentation for a recommendation system project developed to address the needs of Phoenix Incorporated, a Kenyan startup entering the competitive streaming service market. In an era where personalized content recommendations play a pivotal role in user satisfaction and platform revenue, the aim of this project is to construct a recommendation system capable of suggesting 5 movies to users based on their viewing history and popular content trends within the streaming service. By tackling the cold start problem for new users and optimizing recommendation algorithms, this project strives to enhance user engagement and retention while providing valuable insights into data exploration, preprocessing, modeling, and analysis. Explore the contents of this repository to delve into the journey of building a powerful recommendation system for Phoenix Incorporated.

This README.md provides an overview of the project and its segments:
1. [OBJECTIVES](#objectives)
2. [BUSINESS UNDERSTANDING](#business-understanding)
3. [DATA UNDERSTANDING](#data-understanding)
4. [DATA PREPARATION](#data-preparation)
5. [EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)
6. [MODELLING](#modelling)
7. [CONCLUSION](#conclusion)
8. [RECOMMENDATIONS](#recommendations)

## OBJECTIVES
The objectives of this project are:
- To build a recommendation system capable of suggesting 5 movies to users based on their past choices and popular content in the streaming service currently.

- To address the `cold start problem` to provide valuable recommendations to new users with limited interaction history.

- To optimise recommendation algorithms to maximise user satisfaction and platform revenue.

- To implement recommendation system to enhance user engagement and retention.

## BUSINESS UNDERSTANDING

### 2.1 PROBLEM STATEMENT

To build a recommendation system that offers 5 recommendations to a user based on previous content and also what other users with similar interests have watched.

### 2.2 MEASURE OF SUCCESS
The goal is to build a recommendation system that recommends 5 movies to a user based on previous things watched and what other users with similar interests have watched. The measure of success will therefore be a working recommendation system that is able to offer recommendations to new and old users with at least 0.5 RMSE. This is a good starting point. The model can them be improved later based on suggestion from users as Netflix even as a company has been around for more than 10 years, hence it has had time to improve its recommendation systems to almost perfect.

## DATA UNDERSTANDING

In the Data Understanding section, we delve into a comprehensive exploration of the dataset to gain a deeper understanding of its structure and contents. This phase is crucial for setting the foundation for subsequent data preparation, analysis, and modeling steps.

#### General Statement

We begin by providing an overview of the dataset, highlighting its sources, size, and the context in which it was collected. This helps us establish a clear understanding of the data's origins and intended use.

#### Ratings

We specifically examine the ratings data within the dataset, aiming to understand the distribution of user ratings, explore any trends, and identify potential outliers. This analysis is essential as it forms the basis for our recommendation system.

#### Movies

Next, we focus on the movies dataset, exploring details about movie titles, genres, and release years. This information is crucial for enhancing the recommendation algorithm's effectiveness.

#### Links

We investigate the links dataset, which provides essential connections between movies and external sources, potentially enriching our understanding of the movies themselves.

#### Tags

Lastly, we explore the tags dataset, which contains user-generated tags for movies. Understanding user-generated tags can help in refining the recommendation system, enabling it to consider user preferences beyond numerical ratings.

This Data Understanding phase equips us with the necessary knowledge to make informed decisions during the subsequent stages of data preparation, exploratory data analysis, and modeling, ultimately leading to the development of a robust movie recommendation system.

## DATA PREPARATION

The Data Preparation phase involves a series of critical steps to ensure that the dataset is in an optimal state for analysis and modeling. This section outlines the key actions undertaken to clean, transform, and structure the data effectively.

#### Combining Dataframes Using a Common Key

The first step involves combining multiple dataframes using a common key or identifier. This consolidation process aims to create a unified dataset that incorporates relevant information from different sources.

#### Handling Missing Values

Addressing missing data is crucial for maintaining data integrity. In this phase, we identify and implement strategies to handle missing values, such as imputation or removal, to minimize their impact on subsequent analysis.

#### Checking for Duplicates

Duplicate records can distort analysis results and recommendations. We systematically check for and remove duplicate entries within the dataset, ensuring data accuracy.

#### Creating a New Year Column from the Title Column

To enhance our analysis and modeling capabilities, we extract and create a new column representing the release year of movies based on information from the movie titles.

#### Checking for Wrong Datatypes

Ensuring that data types are correct is vital for effective analysis. We review and adjust data types as needed to align with the nature of the variables.

#### Checking for Outliers

Outliers can significantly influence the performance of recommendation algorithms. We identify and handle outliers to prevent them from affecting our models' accuracy.

#### Feature Engineering

Feature engineering involves creating new features or modifying existing ones to capture valuable information. In this phase, we engineer features to enhance the recommendation system's ability to provide relevant suggestions.

The Data Preparation steps collectively prepare the dataset for the subsequent Exploratory Data Analysis and Modeling phases, ensuring that our analysis is based on clean, structured, and well-prepared data.

### EXPLORATORY DATA ANALYSIS

The Exploratory Data Analysis (EDA) phase is a crucial step in understanding the dataset's characteristics, patterns, and relationships. It provides valuable insights into the data's distribution and informs subsequent modeling decisions. In order to do this several steps for both Univariate and Multivariate analysis were taken to further understand our data during modelling. Here is a summary of what was found.

#### Univariate Analysis

- **Number of Movies Released Every Year:** We analysed the number of movies released each year where we found most movies were released in the `90s.`
  ![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/2d88bb26-4634-4f1a-8ab3-de5dd9d5d1b4)
  
- **Number of Movies for Each Genre Released:** We analysed how many movies for each genre were released over the years which were found were `Drama` and `Thriller`
  ![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/68599651-610e-4b12-be3d-2902108609b5)

- **Distribution of the Number of Ratings by Users:** We investigated how ratings are distributed across users, to see if there was bias where one person was making the most ratings were found no bias.
  ![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/32713605-846f-4f23-abd2-9e2bce12f0da)

- **Relationship Between the Age of a Movie and Its Ratings:** We wanted to see if there was a relationship between the age of a movie and the chances of it being rated. Here we found movies in the 90s were the most rated but that's probably due to the fact that most movies were released in the 90s rather than the age of the movie.
  ![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/c4b8ee58-7386-4094-989d-728e48d3dc43)

- **Distribution of Ratings:** We analysed how the ratings were distributed to see how many people gave a certain rating from 1 to 5. Interesting enough we found that  the number of ratings increased with the rating itself.
  ![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/fbe8ad0c-4296-49bc-b13e-5923e149ce0b)

#### Bivariate Analysis
We wanted to see if the relation between features in our dataset. Here are the questions we asked:

- **Correlation Between Release Year and Average Ratings:** We wanted to see if there was a correlation between the age of a movie and its ratings to see if customers favored older movies to newer movies, according to the scatterplot there was no correlation but movies from the `40s` to `80s` had high ratings but this ratings have decreased over a period of time starting from 2000.
![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/df056299-97bd-4eba-a950-bf0d2e8e429e)

- **User Ratings Across Different Movie Genres:** We wanted to see how users rated different genres of movies to see if there was a preference of one type of movie over another. The graph showed that there was no one type of movie favored over the other but rather it was the quality of the movie which determined the rating.
  ![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/74a8c852-8a3a-42df-b959-14b585775aec)

- **Evolution of User Ratings for Specific Genres Over the Years:** We wanted to see if the taste of users has evolved over time or if it had remained constant for specific genres. We found the taste remained almost the same despite a few hiccups here and there except for the `Comedy` genre which was all over the place.
  ![image](https://github.com/DennisWainaina/Phase_4_final_project/assets/116555573/3e7b2108-4fcf-4840-b467-e6fff1d9ce6a)

The EDA phase helped us uncover patterns, trends, and potential relationships within the dataset, providing valuable insights for the subsequent modeling phase. It also informed our understanding of user behavior, genre preferences, and movie popularity, which are essential for building an effective recommendation system.

## MODELLING

The Modeling phase is a critical component of our recommendation system project, where we explore various algorithms and techniques to create an effective movie recommendation model. We've employed several models and approaches to achieve the project's objectives. Here's an overview of the key steps and models used in this phase:

1. **BASE MODEL**
   - Model: Singular Value Decomposition (SVD)
   - RMSE: 0.3917 (Initial Benchmark)
   - *Statement:* In this initial phase, we implemented the basic SVD model to establish a baseline for our recommendation system. This model yielded an RMSE of 0.3917, indicating room for improvement.

2. **MODEL 2**
   - Model: Modified SVD (SVD2) with Hyperparameter Tuning
   - RMSE: 0.7941 (Higher RMSE Despite Tuning)
   - *Statement:* Model 2 involved experimenting with a modified SVD algorithm (SVD2) and fine-tuning its hyperparameters using GridSearch. Despite efforts, this model resulted in a higher RMSE, suggesting it might not be suitable for our dataset.

3. **MODEL 3**
   - Model: Optimized SVD1 with Hyperparameter Tuning
   - RMSE: 0.3466 (Improved Performance)
   - *Statement:* For Model 3, we returned to the original SVD algorithm (SVD1) and optimized it by fine-tuning hyperparameters. This model achieved an improved RMSE of 0.3466, demonstrating better performance.

4. **MODEL 4**
   - Model: K-Nearest Neighbors (KNNBasic)
   - RMSE: 0.5570 (Computationally Intensive)
   - *Statement:* Model 4 explored the K-Nearest Neighbors (KNNBasic) algorithm. However, it proved to be computationally intensive and returned an RMSE of 0.5570, making it less feasible for large datasets.

5. **MODEL 5**
   - Model: Non-Negative Matrix Factorization (NMF) with Hyperparameter Tuning
   - RMSE: 0.6099 (Higher RMSE Compared to SVD1)
   - *Statement:* In Model 5, we implemented Non-Negative Matrix Factorization (NMF) and performed hyperparameter tuning. Unfortunately, this model yielded a higher RMSE of 0.6099 even after `60 mins` of hyperparameter tuning, suggesting it may not be the best fit for our data.

Ultimately, after rigorous testing and experimentation, our best-performing model is the optimized SVD1 model with an RMSE of 0.3466. This model successfully recommends movies to users based on their past choices and popular content, addressing the cold start problem. It serves as an excellent starting point for further improvements and refinements based on user feedback and evolving data.

Our modeling phase demonstrates the importance of selecting the right algorithm and parameters to build an effective recommendation system that enhances user engagement and satisfaction.

## CONCLUSION

In this extensive movie recommendation project, we embarked on a journey to design and implement an effective recommendation system that provides personalized movie suggestions to users based on their preferences and historical interactions. Our endeavor began with a thorough Exploratory Data Analysis (EDA), where we meticulously examined the dataset to extract valuable insights. One notable finding from our EDA was the discovery of a correlation between the release year of movies and their average ratings. Having gained a holistic view of our dataset, we embarked on building a recommendation system. Our journey commenced with a base model rooted in Singular Value Decomposition (SVD). The success of this base model led us to experiment with more sophisticated alternatives, including a modified SVD variant and Non-Negative Matrix Factorization (NMF). In conclusion, this project underscores the critical role of data exploration and algorithm selection in building effective recommendation systems, with our SVD-based model offering the most promising results for our dataset. Continuous improvement, driven by user feedback and scalability considerations, will be essential in further enhancing the recommendation system.


## RECOMMENDATIONS

From the conclusion and EDA here are possible recommendations we can offer:
- **Continuous User Feedback**: Implement a feedback mechanism that encourages users to rate and provide feedback on movie recommendations. This data can be invaluable for fine-tuning the recommendation algorithms over time.

- **Algorithmic Diversity**: Experiment with a variety of recommendation algorithms, including content-based, collaborative filtering, and hybrid approaches. Continuously monitor their performance and adapt the system to use the most effective algorithm for different user segments or scenarios.

- **Scalability and Efficiency**: Consider the scalability of the recommendation system, especially when dealing with large datasets. Explore algorithms and techniques that can handle growing user bases and movie catalogs efficiently.

- **Personalization and Diversity**: Enhance the personalization aspect of the recommendations by incorporating user profiles, historical behavior, and demographic information. Additionally, ensure that the system recommends a diverse set of movies to cater to different user tastes.

- **A/B Testing**: Conduct A/B tests to evaluate the impact of recommendation changes on user engagement and satisfaction. This will help in making data-driven decisions about algorithm adjustments and feature enhancements.

- **Data Quality and Cleansing**: Continuously monitor and clean the data to ensure data quality. Address issues like duplicate entries, missing values, and outliers to prevent them from affecting recommendation accuracy.

- **Privacy and Security**: Implement robust privacy controls to protect user data and adhere to data privacy regulations. Ensure that user profiles and preferences are handled securely.

- **Mobile and Platform Integration**: Extend the recommendation system to various platforms, including mobile apps, smart TVs, and web applications, to maximize user reach and convenience.

- **User Education and Onboarding**: Provide onboarding guidance to users, helping them understand how the recommendation system works and how to make the most of it. Educate them on the benefits of rating and providing feedback.

- **Regular Model Reevaluation**: Periodically revisit and reevaluate the recommendation models. As user preferences evolve, update the models and algorithms to maintain relevance and accuracy.

These recommendations, when implemented, will contribute to the ongoing success and effectiveness of the movie recommendation system, ensuring that it continues to provide valuable and personalized movie suggestions to users. 
**With the successful implementation of the model and extensive EDA done the project is finished, if clients follow these recommendations and use the most successive model as a starting point it will provide a successful platform to build on as they continue on this journey of starting a streaming service. Thank you for reading my README.md**

