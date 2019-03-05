# Project 3 - Barcelona vs Real Madrid - El Clásico de Reddit

# README and Executive Summary


 
#### Project 3: Web APIs & Classification

### Christopher Williams

### DSI 2018
### December 21, 2018



## Contents of project-3 (folder)

README and Executive Summary

Jupyter Workbooks

- DataCollection
---Project 3 - Part 1a - Data Collection Workbook of Submissions.ipynb
---Project 3 - Part 1b - Data Collection Workbook of Comments.ipynb
---Project 3 - Part 1c - Data Combining Submissions and Comments into One Dataframe.ipynb 

- Models
--- Project 3 - Part 2a - Model with Players and Teams Names Included.ipynb
--- Project 3 - Part 2b - Model Using StopWords of Players and Teams Names

- datasets (folder)
--- dfb.csv (dataframe of collected data from Barca subreddit)
--- dfr.csv (dataframe of collected data from realmadrid subreddit)
--- df.csv (main dataframe of collected data)

- Presentation
--- Project 3 - El Clasico de Reddit.pdf
--- Project 3 - El Clasico de Reddit.pptx


## Table of Content of Two Model WorkBooks

Summary of Models
Imports
Data Import
Data Cleaning
Baseline Model
Feature Engineering and transform data with CountVectorizer
Top Words - No Stop Words to See Top Words
Add Regular English Stop Words to See Top Words
Add to Stop Words all Players from last season, Clubs name, and several nicknames for club
Vectorizing on df with CountVectorizer and using custom_stop_extra
Train Test Split
Models Section
Hashing and TF-IDF
TfidfVectorizer Models
TfidfVectorizer and LogisticRegression
Random Forest Models
Word Cloud Generator
End






## Objectives

## Executive Summary

The data science problem we are faced with is to get text data from two subreddits and build classification models to predict if certain data came from the subreddit. I choose comments collected from following 2 subreddits: Barca & realmadrid https://www.reddit.com/r/Barca/ and https://www.reddit.com/r/realmadrid/. FC Barcelona and Real Madrid are futbol clubs based in Spain and have large international fan bases. 

For more information on how data was gathered, see (Part 1: Data Collection Workbook)

We are going to use NLP models and their underlying algorithms to make predictions and score the accuracy of the models. 

To collect the data I used reddit’s API  and pushshift.io’s API to collect submissions and comments from each team's subreddit. I collected 2834 Barca comments and 2747  Real Madrid comments. 

I took the data, cleaned it of any puntuation and then put it into a master dataframe 'df.'

Once the data collection and processing part was cleaned. I created two workbook to include my code for the models. One For "Model with Players and Teams Names Included" and another "Model Using StopWords of Players and Teams Names." As these are Subreddit threads discussing sports by their fans, the players' and teams' names make an enormous difference in the performance of the models accuracy when left in or otherwise excluded. 

For Instance my scores on the following models where the following: 
RandomForestClassifier 
Best cv scores: 
Train: 0.732 without stop words of names and teams | 0.655 with stop words of names and teams 
Test: 0.699 without stop words of names and teams | 0.608 with stop words of names and teams

ExtraTreesClassifier
Best cv scores: 
Train: 0.743 without stop words of names and teams | 0.664 with stop words of names and teams
Test: 0.699 without stop words of names and teams | 0.604 with stop words of names and teams


Top features is players names. Take the names out, accuracy score drops substantially. Regardless due to the nature of comments being so randomly similar within the two subreddits, the scores are harder to predict without those key 109 first and last names and team names. 

With more time I would do the following: model with more model parameters such as ngram features (1,6), put in coaches as stop words, and check out more of the key phrases used by one thread versus the others. 



## Covered in Power Presentation

### The Data Science Process

**Problem Statement**
Create classification models on the Subreddit datasets to predict the class of a comment.

**Data Cleaning and EDA**

**Modeling**

**Evaluation**

**Conclusion**
