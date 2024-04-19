# Youtube Channel-Recommender

Are you dreaming of launching a successful YouTube channel but feeling overwhelmed by the vastness of the platform? Have you ever wondered what makes a YouTube video go viral? Cracking the code for creating consistently popular content can feel like a mystery. But there's a secret weapon at your disposal: YouTube trending video analytics. By analyzing these trends, you can gain valuable insights into what viewers are currently engaging with. You can then leverage this knowledge to tailor your content strategy, identify topics with high potential, and ultimately create videos that resonate with your audience and propel your channel towards success.



**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**

# Table of Content
- [Business Understanding]
- [Data Understanding]
- [Data Analysis]
- [Recommendation Engine]
- [Conclusion and Future Consideration]
- [References]
- [For More Information]

**-- Reccomended changes to wording below to accuratly match exsisting content titles. Also added subcatagories to a few sections for our project within the README file --**

# Table of Content
- [Business Understanding]
- [Data Understanding]
- [Data Analysis]
- [Recommendation Engine]
- [Conclusion and Future Consideration]
- [For More Information]
- [References]


# Business Understanding 

YouTube operates in the field of digital media and online video streaming. It provides a platform for users to upload, share, and view a wide variety of video content, including entertainment, educational, informational, and user-generated videos. As one of the world's largest online video platforms, YouTube facilitates content creation, distribution, and consumption, making it a significant player in the digital media landscape.

In this project, we're on a mission to empower aspiring YouTube and digital marketing enthusiasts with powerful recommendation engines. Whether you're dreaming of launching your own YouTube channel or diving into the world of digital marketing, we've got you covered. Through careful analysis of YouTube's top views and trends, coupled with advanced data-driven techniques, we'll craft personalized recommendations tailored to your unique goals and interests. From content strategy to audience engagement, let us guide you on the path to success in the dynamic realm of online content creation and marketing.

# Data Understanding 

The dataset that I’m working with is a snip of US Youtube data from Aug 2020 to Apr 2024. Our YouTube dataset maintain a list of the top trending videos on the platform. According to Variety magazine, “To determine the year’s top-trending videos, YouTube uses a combination of factors including measuring users interactions (number of views, comments and likes). 

# Data Analysis

After processing the data and doing some exploratory analysis, here are the most interesting features of this dataset:

**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**

- After analyzing the dataset, several key findings emerge. The top 10 fastest viral YouTube videos within the first 24 hours highlight the potential for rapid audience engagement. Understanding trends in the number of trending videos by day of the week offers insights into optimal upload times. The top 10 channels by total view count showcase successful strategies for building a large audience. Analysis of average views by month reveals seasonal viewership patterns, while common tags provide guidance for content optimization. Metrics such as total views and comments by channel and video category offer comprehensive insights into audience engagement levels and content preferences. Additionally, examining the frequency of posting by top channels and metrics like total comments, dislikes, and likes by video views provides valuable strategies for maximizing audience interaction and content effectiveness.


**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**

- There is a strong positive correlation between likes and view count.
- On average, videos with disabled comments and ratings have significantly fewer dislikes compared to those with enabled comments and ratings. Additionally, despite disabled engagement features, such videos still garner a higher view count. This correlation may indicate that limiting user feedback could lead to a more positively perceived content, potentially driving higher engagement in terms of likes and views. However, further analysis is needed to ascertain causation and account for other factors influencing viewer engagement.
  
- Top 5 Categories are 
- Top 5 Tags are:
- Top 2 industries are gaming and sport industries

![Snip20240417_1](https://github.com/mahshid-alinejad/Project-1/assets/158861742/b973a822-54c8-4027-8864-ff767554b98e)

  

# Recommendation Engine

## Recommendations based on Popularity to a New User

**-- Reccomended changes to above wording below --**

**Recommendations based on popularity**

As the name suggests it recommends based on what is currently trending/ popular across the site. This is particularly useful when you don't have past data as a reference to recommend product to the user. It is not tailor fit for any particular group of audience.

These are the most popular categories
These are the most popular tags
These are ......

**-- Reccomended changes to above wording below --**

**This method is used to provide recomendations based on what is currently trending/ popular across the site. This is particularly useful when historical data is unavaiable for reference to the user. This data ouput is not tailored for any particular group or audience.**

**These are the most popular categories
These are the most popular tags
These are the most viewed videos
These are the most liked videos
These are the most comented videos
etc...**

**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**


## Recommendations based on View Count and Total Likes and Categories and Tags

**-- Reccomended changes to above wording below --**

**Recommendations based on View Count, Total Likes, Categories, and Tags**

Content based recommendation system is certainly good if we want to recommend suggestions based on features like View Count and Total Likes and Categories and Tags ....

**-- Reccomended changes to above wording below --**

**A content based recommendation system is certainly good if you want to recommend suggestions based on features like: View Count, Total Likes, Categories, Tags, etc.**

**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**

Some limitations of content based filtering are that it can only make recommendations based on existing interests of the user, it does not consider the fact that what do other users think of an item

**-- Reccomended changes to the above wording below --**

**A couple of limitations when using content based filtering are: It can only make recommendations based on existing interests of the user. It does not consider  what other users think of an item.**

## Collaborative Filtering 

### Item-Based Collabrative Filtering
**NEEDS OUR INPUT**

The main idea behind these methods is to use other users’ preferences and taste to recommend new items to a user. The usual procedure is to find similar users (or items) to recommend new items which where liked by those users, and which presumably will also be liked by the user being recommended.

**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**

### Collaborative Filtering Model Based on User Ratings

#### Best Performing Model
**NEEDS OUR INPUT**

**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**

In this section, I chose **RMSE (Root Mean Squared Error)** as our evaluation metrics . We got the best RMSE result with SVDpp. Since SVDpp takes longer time to train compared to the naive SVD.So, I chose to optimize the SVD model.

Finally, after optimizing the SVD model , I've gotten **0.8525** RMSE score .**That would mean the estimated ratings on average are about 0.8525 higher or lower than the actual ratings, on a 0 to 5 scale**

After optimizing and predicting rating on model, I got 10 recommendations

**img align="center" width="600" height="400" src=' INSERT IMAGE PATH HERE '**

These look like pretty good recommendations. It’s good to see that, although I didn’t actually use the genre of the movie as a feature, the truncated matrix factorization features “picked up” on the underlying tastes and preferences of the user. I’ve recommended some comedy, drama, and romance movies — all of which were genres of some of this user’s top rated movies.

# Conclusion and Future Consideration
**NEEDS OUR INPUT**

In this notebook different recommendation approaches of content and collaborative filtering has been discussed.

First, I did exploratory data analysis then I started with content based filtering to recommend movie to new user based upon genre and movie popularity or the average ratings given by other users in the database.

I then progressed collaborative filtering based engines which try to find similar movies or users to make their predictions. After assessing models on RMSE metric, I found SVD++ to be the most accurate model but since SVD++ hyperparameters tuning time consuming I decided to go with SVD model tuned hyperparameters by using GridSearchCV

Finally, I made a recommendation engine which recommends 10 movies to specific user by using SVD model. And I added filtering options for genre and minimum number of ratings to make recommendations more accurate

There is a lot of potential to do but in the future, deep learning based recommender system can be built to enhance the performance and provide better recommendations to user.

## Our Advice To Future Users
**NEEDS OUR INPUT**

- Collaborative Filtering Recommender Engine more effectively when it comes to recommend movies based on other users' preference but It doesn't solve the cold start problem. To help solve this problem we can use hybrid model of our naive recommendation engine and the model based recommendation engine.

- Most popular genres will be a relevant aspect to take into account when building the content based recommender.

- We optimized SVD model to prevent time consuming and cost but Optimizing SVDpp can be more efficient since SVDpp is an extension of SVD model which deals with both explicit feedback an implicit feedback


# For More Information
**NEEDS OUR INPUT**

If you have any questions, feel free to contact us:

Romario Esparza: #Email and/or #Social
Mahshid Alinejad: #Email and/or #Social
Ben Cross: #Email and/or #Social
Stephen Martinez: #Email and/or #Social

# References

## Data Source
**Kaggle.com**
    *https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset/data*


### Repository Structure
**NEEDS OUR INPUT AFTER GITHUB CLEANUP**
    
```
├── xxxxxx
├── xxxxxx
├── xxxxxx
├── xxxxxx
├── xxxxxx
└── README.md
```
