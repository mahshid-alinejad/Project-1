# Youtube Channel-Recommender

1 Are you dreaming of launching a successful YouTube channel but feeling overwhelmed by the vastness of the platform? Have you ever wondered what makes a YouTube video go viral? Cracking the code for creating consistently popular content can feel like a mystery. But there's a secret weapon at your disposal: YouTube trending video analytics. By analyzing these trends, you can gain valuable insights into what viewers are currently engaging with. You can then leverage this knowledge to tailor your content strategy, identify topics with high potential, and ultimately create videos that resonate with your audience and propel your channel towards success.



<img align="center" width="900" height="300" src='images/MovieLens.png'>

# Table of Content
- [Business Understanding]
- [Data Understanding]
- [Data Analysis]
- [Recommendation Engine](
- [Conclusion and Future Consideration]
- [References]
- [For More Information]

# Business Understanding 

YouTube operates in the field of digital media and online video streaming. It provides a platform for users to upload, share, and view a wide variety of video content, including entertainment, educational, informational, and user-generated videos. As one of the world's largest online video platforms, YouTube facilitates content creation, distribution, and consumption, making it a significant player in the digital media landscape.

Through careful analysis and strategic planning, we help businesses identify opportunities for growth and engagement across various social media channels. Whether it's developing a cohesive content strategy, optimizing advertising campaigns, or enhancing brand visibility, we are committed to delivering measurable results that drive business success.

In this project, we're on a mission to empower aspiring YouTube and digital marketing enthusiasts with powerful recommendation engines. Whether you're dreaming of launching your own YouTube channel or diving into the world of digital marketing, we've got you covered. Through careful analysis of YouTube's top views and trends, coupled with advanced data-driven techniques, we'll craft personalized recommendations tailored to your unique goals and interests. From content strategy to audience engagement, let us guide you on the path to success in the dynamic realm of online content creation and marketing.

# Data Understanding 

By analyzing audience engagement, content effectiveness, and overall impact in the digital landscape, we can gain valuable insights into the effectiveness of our social media strategies and make data-driven decisions to optimize performance and achieve business objectives.

1. Audience Engagement:Comments, Likes and Shares, Click-Through Rates (CTR: measures the percentage of users who click on a link or call-to-action within the content. )
2. Content Effectiveness:Title, Tags, Description, View Count, Consistency, Publishing Frequency
3. Overall Impact in the Digital Landscape:View counts and share counts
By analyzing these factors and leveraging available data, you can gain valuable insights into content effectiveness and overall impact in the digital landscape, enabling you to optimize social media strategies and achieve business objectives.

The dataset that I’m working with is a snip of US Youtube data from Aug 2020 to Apr 2024. Our YouTube dataset maintain a list of the top trending videos on the platform. According to Variety magazine, “To determine the year’s top-trending videos, YouTube uses a combination of factors including measuring users interactions (number of views, comments and likes). 



# Data Analysis

We conducted data analysis by sorting our dataset based on "view counts" to identify trends and patterns in video popularity.

<img align="center" width="900" height="300" src='images/Distribution of Genres.png'>

- We found out top trending videos from Aug 2020 to Apr 2024,as well as which day of the week and what time of the day are peak times. So if someone needs our consultant on best days to post and which hour is the best hour to post.  There is also a strong positive correlation between likes and view count. Our data represents that top industries in Youtube channel are gaming, sports and News. 

We 


- After analyzing the dataset, several key findings emerge. The top 10 fastest viral YouTube videos within the first 24 hours highlight the potential for rapid audience engagement. Understanding trends in the number of trending videos by day of the week offers insights into optimal upload times. The top 10 channels by total view count showcase successful strategies for building a large audience. Analysis of average views by month reveals seasonal viewership patterns, while common tags provide guidance for content optimization. Metrics such as total views and comments by channel and video category offer comprehensive insights into audience engagement levels and content preferences. Additionally, examining the frequency of posting by top channels and metrics like total comments, dislikes, and likes by video views provides valuable strategies for maximizing audience interaction and content effectiveness.


<img align="center" width="900" height="300" src='images/Distribution of Ratings.png'>

- On average, videos with disabled comments and ratings have significantly fewer dislikes compared to those with enabled comments and ratings. Additionally, despite disabled engagement features, such videos still garner a higher view count. This correlation may indicate that limiting user feedback could lead to a more positively perceived content, potentially driving higher engagement in terms of likes and views. However, further analysis is needed to ascertain causation and account for other factors influencing viewer engagement.
  


![Snip20240417_1](https://github.com/mahshid-alinejad/Project-1/assets/158861742/b973a822-54c8-4027-8864-ff767554b98e)

  

# Recommendation Engine

## Recommendations based on Popularity to a New User

Our data shows that Saturday are the best days to go viral and the Youtube video postings are usually go viral after 9 hrs of publishing. According to our analysis it also takes an average 5 days for videos to trend. Our data represents that top industries in Youtube channel are gaming, sports and News. People blogging has been one of the top brands which might help increase the sale for companies with consumer goods products such as skin care, clothing, etc.,

Based on these datas we can recommond people who just want to start a business which product categories have the most views and if gaming for example top industry maybe selling a toy can bring a high sales by posting on Youtube as a markeing platform. 
We dived deeper into the data and we conducted a research on top categories based on higherst view counts to figure out what industries under consumer goods products will also thrive on Youtube platform as their digital marketing strategy, pet products, cars, traveling 



The more engagement involves things such as leaving the comment section for example always open, also there is a strong relation between using more tags and getting more views.  Channels with higher frequency of posting get more views as well. 

As the name suggests it recommends based on what is currently trending/ popular across the site. This is particularly useful when you don't have past data as a reference to recommend product to the user. 


<img align="center" width="600" height="400" src='images/get recommendation based on popularity.png'>

![Snip20240420_8](https://github.com/mahshid-alinejad/Project-1/assets/158861742/c1a1b9c1-0ab8-4671-a7a3-72f59fb8825e)



## Collaborative Filtering 

### Item-Based Collabrative Filtering

The main idea behind these methods is to use other users’ preferences and taste to recommend new items to a user. The usual procedure is to find similar users (or items) to recommend new items which where liked by those users, and which presumably will also be liked by the user being recommended.

<img align="center" width="700" height="400" src='images/movie similarity item based .png'>

### Collaborative Filtering Model Based on User Ratings

#### Best Performing Model

<img align="center" width="900" height="400" src='images/Comparison of Models.png'>

In this section, I chose **RMSE (Root Mean Squared Error)** as our evaluation metrics . We got the best RMSE result with SVDpp. Since SVDpp takes longer time to train compared to the naive SVD.So, I chose to optimize the SVD model.

Finally, after optimizing the SVD model , I've gotten **0.8525** RMSE score .**That would mean the estimated ratings on average are about 0.8525 higher or lower than the actual ratings, on a 0 to 5 scale**


After optimizing and predicting rating on model, I got 10 recommendations

<img align="center" width="900" height="400" src='images/Top 10 Recommendations.png'>

These look like pretty good recommendations. It’s good to see that, although I didn’t actually use the genre of the movie as a feature, the truncated matrix factorization features “picked up” on the underlying tastes and preferences of the user. I’ve recommended some comedy, drama, and romance movies — all of which were genres of some of this user’s top rated movies.

# Conclusion and Future Consideration

In this notebook different recommendation approaches of content and collaborative filtering has been discussed.

First, I did exploratory data analysis then I started with content based filtering to recommend movie to new user based upon genre and movie popularity or the average ratings given by other users in the database.

I then progressed collaborative filtering based engines which try to find similar movies or users to make their predictions. After assessing models on RMSE metric, I found SVD++ to be the most accurate model but since SVD++ hyperparameters tuning time consuming I decided to go with SVD model tuned hyperparameters by using GridSearchCV

Finally, I made a recommendation engine which recommends 10 movies to specific user by using SVD model. And I added filtering options for genre and minimum number of ratings to make recommendations more accurate

There is a lot of potential to do but in the future, deep learning based recommender system can be built to enhance the performance and provide better recommendations to user.

# Recommendations

- Collaborative Filtering Recommender Engine more effectively when it comes to recommend movies based on other users' preference but It doesn't solve the cold start problem. To help solve this problem we can use hybrid model of our naive recommendation engine and the model based recommendation engine.

- Most popular genres will be a relevant aspect to take into account when building the content based recommender.

- We optimized SVD model to prevent time consuming and cost but Optimizing SVDpp can be more efficient since SVDpp is an extension of SVD model which deals with both explicit feedback an implicit feedback


# For More Information

If you have any additional questions, feel free to contact me at ysm.cebeci@gmail.com or connect with me on [LinkedIn](https://www.linkedin.com/in/jade-cebeci/). Also, be sure to check out my [blogpost](https://medium.com/@ysm.cebeci/getting-started-with-recommender-systems-collobrative-filtering-e1fe9141c055) for more insights on building a personalized recommendation engine using collaborative filtering techniques.


# Repository Structure

    
```
├── images
├── ml-latest-small
├── the deliverables
├── EDA_and_Data_Cleaning.ipynb
├── Movie_Recommender_Modeling.ipynb
└── README.md
```



Sources: https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset/data
