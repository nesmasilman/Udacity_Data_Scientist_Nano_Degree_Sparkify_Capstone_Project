# Project Title
Sparkify Capstone Project

# Table of contents
* Introduction
* Scope
* Datasets
* Technologies
* Outcome
* Resources

# Introduction
This project explores a music streaming application called "Sparkify". We have a dataset that contains data related to the app. users and their activities within the app. In this project, we will be working on a small subset of the data to explore different features and build a machine learning model to predict users churn.

We can define churn as the activity when a user submits a "Cancellation Confirmation" request. Predicting users churn will help us try to understand the reasons (features) that contributes to their churn decision and try to overcome it. We can also make tailored offers/promotions for the predicted churn users to retain them.

# Scope
By exploring this dataset, we will be looking for answers for the below 3 questions:

1- Extract the listings with the highest # of reviews (top 10). Which one got the highest % of positive reviews?

2- What are the top 3 most frequent neighbourhoods or zipcodes in Boston? (zipcodes with highest number of listings).

3- How the price correlates to the property_type? What types are the most expensive?

# Datasets
The Zipfile (archive (3).zip) contains 3 csv files

Listings: including full descriptions and average review score
Reviews: including unique id for each reviewer and detailed comments
Calendar: including listing id and the price and availability for that day

# Technologies
This project uses Python 3.10.9 version

# Outcome
After exploring the datasets, here are the answers to our questions:

1- Extract the listings with the highest # of reviews (top 10). Which one got the highest % of positive reviews?

By exploring the data, we found that listing_id 815639 has the highest % of positive reviews (97.15%)

2- What are the top 3 most frequent neighbourhoods or zipcodes in Boston? (zipcodes with highest number of listings).

The highest zipcodes were ['02116', '02130', '02118']. We started by exploring the neighbourhood column, but it had around 15% missing values with no other source to impute the missing values, so we considered the zip code column

3- How the price correlates to the property_type? What types are the most expensive?

It was found that Guesthouse has the highest average price, but since we only had 1 record with this type, we moved to the next highest type which was "Boat"

# Resources
The dataset was obtained from Kaggle link https://www.kaggle.com/datasets/airbnb/boston
