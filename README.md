# GA-Project-3

# Problem Statement
We are a team of Data Analyst at ABC consultancy working together with CHAT to improve their webCHAT email platform for youths to get support for emotional concerns.<br>

Based on the emails received from chat@mentalhealth.sg, we want to accurately assign them into "anxiety" or "depression" category and allow the counsellors to provide them the necessary support and resources.<br>

This project aims to:<br>
(i) Use the reviews from Reddit for r/Anxiety and r/depression and apply Naive Bayes, K-Nearest Neighbors and Logistic Regression modelling to predict if they fall under the anxiety or depression subreddit.<br>
(ii) Find out the words commonly used by both subreddits.

# Background

Due to COVID-19, it resulted in a large group of Singaporeans experiencing anxiety or depression - 1 in 3 adults anxious, depressed. Younger adults, aged 35 and under, were more likely to experience psychological distress than those over the age of 35 due to their greater access to COVID-19 information through the media ([*source*](https://www.duke-nus.edu.sg/allnews/covid-19-1-in-3-adults-anxious-depressed)).<br>

CHAT is the Centre of Excellence for Youth Mental Health in Singapore, which have been helping and supporting young people with mental health concerns since 2009. CHAT runs a national youth mental health outreach and assessment service for youth and young adults aged 16 to 30 ([*source*](https://www.imh.com.sg/CHAT/Pages/default.aspx)).<br>

Young adults in Singaporeans who have experienced psychological distress due to COVID-19 may seek platforms such as CHAT to receive support. Improvements made to CHAT's webCHAT email platform would accurately identify if the subject was experiencing anxiety or depression and allow for counsellors to provide the necessary support and resources to these youths.

# Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|subreddit|object|anxiety.csv/depression.csv|Type of Subreddit|
|title|object|anxiety.csv/depression.csv|Title of Post|
|selftext|object|anxiety.csv/depression.csv|Description of Post|

# Summary of Analysis
Words such are "feel like", "dont know", "anyone else", "dont want" and "mental health" can be seen repeated in both subreddits. <br>

We identified that the Logistic Regression model using TF-IDF-unigram vectorization performed the best out of all the models with a accuracy of 88%, f1-score of 88% and AUC of 0.95.

# Conclusion/Recommendations
The aim of the project was to come up with a model which can predict whether a post from reddit was from the anxiety or depression subreddit and identify words commonly used by both communities by analysing the words from the title and description of these posts.<br>

Given that both condition are psychologial conditions which can be fairly closely interlinked, words such are "feel like", "dont know", "anyone else", "dont want" and "mental health" can be seen repeated in both subreddits.<br>

Through our modelling, we identified that the Logistic Regression model using TF-IDF-unigram vectorization performed the best out of all the models with a accuracy of 88% (without K-fold Cross Validation), f1-score of 88% and AUC of 0.95.<br>

We believe our model can be implemented into CHAT's webCHAT email platform to accurately identify if the subject was experiencing anxiety or depression and allow for counsellors to provide the necessary support and resources to these youths.<br>

Limitations: <br>
- Given that the words used by both the anxiety and depression communities may be fairly similar, there might be a limitation at how well our model can make prediction with high accuracies (>95%). Hence, our recommendations as per point 2 below.

Recommendations: <br>
1. As there are many other pyschological conditions that different subjects may be suffering from, we can perhaps include posts from other subreddits in our studies to improve our model to be able to predict other conditions.
2. We can refer to posts from other platforms and forums to improve our model's accuracy with more variation in data sources.
