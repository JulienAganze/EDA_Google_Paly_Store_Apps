
# Google Play Store apps Analysis
## Exploratory Data Analysis Project
### Brief introduction
This project is related to the analysis of apps available on google playstore with the aim of drawing insights to be made available for any investor who will be willing to invest in app development.

## introduction to data
The data we are going to work with is made of two dataset obtained from Kaggle in csv formats, googleplaystore.csv containing all information related to each and evry specific app, and the second dataset googleplaystore_user_reviews.csv containing all informating related to reviews made for some apps

### a) googleplaystore dataset

Let us define what information the columns contain based on our inspection play_store dataframe has 10841 rows and 13 columns. The 13 columns are identified as below:
* **App** - gives the name of the application with a short description (optional).
* **Category** - gives the category the app belongs to.
* **Rating** - contains the average rating the respective app received from its users.
* **Reviews** - provides the total number of users who have given a review for the application.
* **Size** - tells us about the size an application is occupying on the mobile phone.
* **Installs** - provides the total number of installs/downloads for an application.
* **Type** - tells whether an app is free to use or paid.
* **Price** - gives the price payable to install the app. For free type apps, the price is zero.
* **Content Rating** - gives information about age restriction for a specific app.
* **Genres** - tells us about the various other categories to which an application can belong.
* **Last Updated** - gives information about  when last the application was updated.
* **Current Ver** - informs us the current version of the application.
* **Android Ver** - informs us about the android version which can support the application on its platform.

### b) googleplaystore_user_reviews dataset

User_reviews dataframe has 64295 rows and 5 columns. The 5 columns are identified as follows:

* **App:** has the names of the different apps with a short description.
* **Translated_Review:** contains the English translation of the review dropped by the user of the app.
* **Sentiment:** gives the attitude/emotion of the writer. It can be ‘Positive’, ‘Negative’, or ‘Neutral’.
* **Sentiment_Polarity:** provides the polarity of the review. Its range is [-1,1], where 1 means ‘Positive statement’ and -1 means a ‘Negative statement’.
* **Sentiment_Subjectivity:** This value gives how close a reviewers opinion is to the opinion of the general public. Its range is [0,1]. Higher the subjectivity, closer is the reviewers opinion to the opinion of the general public, and lower subjectivity indicates the review is more of a factual information.

## General Project Overview
To perform the required studies we will follow the following steps:

#### 1. Importing data into the dataframe
This is done using pandas [read_csv](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_csv.html) method. And all needed information about how to use this can be obtained from the later provided link.
#### 2. Collecting basic information about the dataset
I need to need how the data looks like for me to be able to make sens out of it. SO for this reason we will explore additional pandas function like [head](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.head.html) used to look at data in a tabular form, [describe](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.describe.html) performs descriptive statistics, [isnull](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.isnull.html) used to find out if there are null values in different columns
#### 3. Organizing, Cleaning and Completing the data
After knowing how our data looks like, the next step will now bw about dealing with missing values. And for this purpose the following operations will be performed. For this the following two actions are going to be taken\
 ● Dealing with NaN values by eitheir deleting them or replacing them. And for the case of replacing them, we will generally replacing numeric values by either mean or mode values\
 ● Changing the datatypes of some columns to allow us carrying out more detailed analysis 

#### 4. Problem definition
In our study we will be answering the following questions using the two available datasets.\
 ● What are the top categories on Play Store?\
 ● Are majority of the apps Paid or Free?\
 ● How importance is the rating of the application?\
 ● Which categories from the audience should the app be based on?\
 ● Which category has the most no. of installations?\
 ● How does the count of apps varies by Genres?\
 ● How does the last update has an effect on the rating?\
 ● How are ratings affected when the app is a paid one?\
 ● How are reviews and ratings co-related?\
 ● Lets us discuss the sentiment subjectivity.\
 ● Is subjectivity and polarity proportional to each other?\
 ● What is the percentage of review sentiments?\
 ● How is sentiment polarity varying for paid and free apps?\
 ● How Content Rating affect over the App?\
 ● Does Last Update date has an effects on rating?\
 ● Distribution of App update over the Year.\
 ● Distribution of Paid and Free app updated over the Month.


### Project details
All the project details and analysis will be in the project notebook [Google Apps Store Analysis](https://github.com/JulienAganze/EDA_Google_Play_Store_Apps/blob/master/Play_Store_Apps_analysis.ipynb)
![Sentiment](https://github.com/JulienAganze/EDA_Google_Play_Store_Apps/blob/master/Sentiment.png)
### Used data source
The two dataset we used in this project can be obtained from Kaggle [Google Play Store Apps](https://www.kaggle.com/datasets/lava18/google-play-store-apps?datasetId=49864)

## Used libraries
The following libraries will be used in this project

● [Numpy](http://www.numpy.org/)
NumPy is a library for the Python programming language, adding
support for large, multi-dimensional arrays and matrices, along with a
large collection of high-level mathematical functions to operate on
these arrays.

● [Pandas](https://pandas.pydata.org/)
Pandas is a python package providing fast, flexible, and expressive
data structures designed to make working with “relational” or “labeled”
data both easy and intuitive. It aims to be the fundamental high-level
building block for doing practical, real world data analysis in Python.
Additionally, it has the broader goal of becoming the most powerful and
flexible open source data analysis / manipulation tool available in any
language. It is already well on its way toward this goal.

● [Seaborn](https://seaborn.pydata.org/)
Seaborn is a Python data visualization library based on matplotlib. It
provides a high-level interface for drawing attractive and informative
statistical graphics.

● [Matplotlib](https://matplotlib.org/)
Matplotlib is a Python 2D plotting library which produces publication
quality figures in a variety of hardcopy formats and interactive
environments across platforms.

● [Datetime](https://www.programiz.com/python-programming/datetime)
Python has a module named datetime to work with dates and times.
It provides a variety of classes for representing and manipulating dates and times, as well as for formatting and parsing dates and times in a variety of formats.
