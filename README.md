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

# Define
Remove all observations in the feed_clean dataset that have values in the rows in_reply_to_status_id or retweeted_status_id. Then remove those two columns plus retweeted_status_user_id, retweeted_status_timestamp and in_reply_to_user_id

In order to have observational units in their own table, we need to split the feed_clean data-set into a tweets table and a dogs table. This is a design decision because there are many several tweets that include information and ratings for more than one dog. Ratings and dog stages refer to dogs, whereas retweets an likes are related to the tweets.

# Resources
Pandas sort_values(): http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.sort_values.html
Sort values issue in SO: https://stackoverflow.com/questions/44123874/dataframe-object-has-no-attribute-sort
Reading and writing JSON to a file: https://stackabuse.com/reading-and-writing-json-to-a-file-in-python/
SQL Alchemy: https://www.sqlalchemy.org/
Pillow Documentation: https://pillow.readthedocs.io/en/stable/
API tutorial of Mediawiki: https://www.mediawiki.org/wiki/API:Tutorial
Requests Documentation: http://docs.python-requests.org/en/master/user/intro/
Glob documentation: https://docs.python.org/3/library/glob.html
Python Files I/O: https://www.tutorialspoint.com/python/python_files_io.htm
Assessing a tweet with only its ID: https://www.bram.us/2017/11/22/accessing-a-tweet-using-only-its-id-and-without-the-twitter-api/
Reading and writing files in Python: https://www.pythonforbeginners.com/files/reading-and-writing-files-in-python
Test for a pattern in a Pandas dataframe: https://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.str.contains.html
Tidy data: https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html
Imputation concepts for filling missing data: https://en.wikipedia.org/wiki/Imputation_(statistics)
Melt function in pandas: https://pandas.pydata.org/pandas-docs/version/0.23.4/generated/pandas.DataFrame.melt.html#pandas.DataFrame.melt
Commenting several lines of code in Jupyter Notebooks: https://stackoverflow.com/questions/29885371/how-do-i-comment-out-multiple-lines-in-jupyter-ipython-notebook
Extracting specific columns into a new dataframe: https://stackoverflow.com/questions/34682828/extracting-specific-selected-columns-to-new-dataframe-as-a-copy
How to iterate through a pandas series: https://stackoverflow.com/questions/16476924/how-to-iterate-over-rows-in-a-dataframe-in-pandas and https://stackoverflow.com/questions/43222878/iterate-over-pandas-dataframe-and-update-the-value-attributeerror-cant-set-a
Work with strings in pandas: https://pandas.pydata.org/pandas-docs/stable/text.htm
Merging datasets in pandas: https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.merge.html
Pandas .isin() function: https://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.isin.html
Using .loc and .iloc to slice in pandas: https://www.shanelynn.ie/select-pandas-dataframe-rows-and-columns-using-iloc-loc-and-ix/
