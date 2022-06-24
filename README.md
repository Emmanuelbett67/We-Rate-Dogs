# We-Rate-Dogs
A Data-Wrangling project by me as part of Udacity's Data Analysis Nanodegree
# Introduction
This project makes part of the coursework leading to Udacity's Data Analysis Nanodegree. Its objective is to demonstrate skills for the Data Wrangling phase of the Data Analysis Process. Data Wrangling is a key part in analytics, and is typically described as the one where analysts and data scientists spend the most part of their time.

The project gathers data from different sources related to the WeRateDogs twitter account, which posts and rates photos of folowers' dogs. After assessing and cleaning the data, reports are written to communicate the results of an initial analysis.
# Gather
The first step of the wrangling process is to obtain data. For this project, we will work with different sources:

- a file in hand with data about each tweet by WeRateDogs, provided by Udacity
- a file downloaded programatically, with breed predictions for each dog
- additional data about each tweet (retweets and fav's), retrieved from Twitter's API

Retrieve additional data from Twitter APIs, for each of the tweets in twitter-archive-enhanced.csv

Each tweet's retweet count and favorite ("like") count at minimum, and any additional data you find interesting. Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file called tweet_json.txt file. Each tweet's JSON data should be written to its own line. Then read this .txt file line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count.

# Assess
Assessing is the process of checking the data sets for two things: quality issues and lack of tidiness. Data that has quality issues has problems with its contents: missing, corrupted, inacurate, duplicate or incorrect data. This is called "dirty data". In the contrary, "untidy" or "messy" data has specific structural issues.

You look for these issues in two ways: visually and programatically. When you detect an issue you document it, to make cleaning easier. You don't write yet how to clean the data, but only state the observation.

- Visual assessment is great for getting acquainted with the data and understanding what it is all about.
- Programatical Assessment, after assessing visually the three datasets and identifying several tidiness issues, we now go deeper using Programatic Assessment.

# Clean
Cleaning the data is the third and last step in the data wrangling process. The issues that were identified are solved programatically, in three steps: Define, Code and Test. We begin by creating copies of each of our three datasets
