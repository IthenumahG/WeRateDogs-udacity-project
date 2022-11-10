### Introduction  
This is a project done in fulfilment of the requirements of the Udacity nanodegree. In this project, I will be using Python and its libraries to gather data from variety of sources and in variety of formats, access the quality and tidiness of the gathered data, and then proceed to clean it.
This project aims to bring to fore the utilisation of all that was learnt in the Data wrangling module of the nanodegree.  

The dataset I will be wrangling, analyzing, visualising and drawing insights from, is the tweet archive of a Twitter account [@dog_rates](https://twitter.com/dog_rates) that rates people's dogs with a humorous comment about the dog. The ratings of these dogs as seen in the Twitter account almost always have a denominator of 10, while the nemurator has rating mostly above 10. At the end of this project I hope to pose and answer some questions regarding the datasets worked with and draw some insights from such answers.  


### Data Gathering  
Udacity in collaboration with WeRateDogs (the twitter account whose tweets I will be analysing), this archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. For the purpose of this project, three (3) datsets will be needed; the WeRateDogs Twitter archive, the tweet image predictions and additional data from the Twittwer API.  

### Data Wrangling Process 
After successfully gathering the three (3) datasets needed for my analysis, the next step is to visually and programatically access them for quality and tidiness issues. Pandas functions like *head*, *info*, *describe*, and *sample* were employed in determining some of the datasets issues, these are;  

#### Quality issues  

* tweet_id is **int** instead of **string**      
* Nulls represented as "None" in the dataset.
* Wrong dog names like "a", "an", "my", "unacceptable" etc in the **name** column.  
* **timestamp** is string instead of datetime type.
* For the purpose of this project we are only interested in original tweets, therefore retweets and in_reply data have to be removed.  
* Columns like **expanded_urls** and **source** not required for my analysis.  
* tweet_id is **int** instead of **string**.  
* Columns **p1**, **p2**, and **p3** has values starting with both upper and lower cases.  
* Missing **tweet_id**s values.  
* Some columns not properly named, that is not descriptive. 
* **id** column is **int** instead of **string**.  
* **id** column should be "tweet_id".  

#### Tidiness issues 

* **doggo**, **floofer**, **pupper**, and **puppo** columns should be in one column "dog_stage"  
* Combine all three dataframes into one dataframe for analysis.  

### Data Cleaning  
After highlighting the quality and tidiness issues in the access phase of the project, I proceeded to cleaning the issues documented using the define-code-test method. But not without first making copies of the original datasets, merging individual pieces datasets into a single master pandas Dataframe named **clean_twitter_archive** I also made sure to first deal with the tidiness issues as it is best practice.  

### Analysis   
After I had adequately dealt with the quality and tidiness issues documentated in the accessing phase of the project, I then posed some questions whose answers I used in analysing the cleaned master dataset. These questions are;    
* What is the relationship of the dog stages to favorite count and retweet count?  
* Which are the most ranked and least ranked dog stages?  
* What are the success rate of the algorithm predictions.  

### Insights  
* Clear positive corelation between the Dog stage and the number of likes and retweets a certain tweet gets.
* The people that engage with the WeRateDogs twitter page almost always have a contrary opinion of its rating of the dogs.  
* Algorithm's predictions determining if image tweeted is a dog are mostly correct.  

### Conclusion  
The goal of this project was wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. This project exhaustively covers all the data wrangling processes; gathering, accessing and cleaning. A lot more insights can be drawn from the data provided, but that will involve more data cleaniing and manipulation. Therefore my findings are limited aand also tentative as it will require more in-depth analysis to give more concrete insights of the data.