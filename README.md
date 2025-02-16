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

# Scope
By exploring this dataset, we will be trying to predict churn cases. We can define churn as the activity when a user submits a "Cancellation Confirmation" request. Predicting users churn will help us try to understand the reasons (features) that contributes to their churn decision and try to overcome it. We can also make tailored offers/promotions for the predicted churn users to retain them.

# Datasets
We are using a small subset from our main dataset. Our subset name is called mini_sparkify_event_data.json 

Columns Description:

* ts : timestamp, when this event was recorded in miliseconds
* userId : identifier unique for each user, can be empty
* firstname : firstname of user, like “Colin”
* lastname : lastname of user, like “Freeman”
* location : city like “Bakersfield, CA”
* gender : “F” for female, “M” for male
* registration : timestamp of subscription
* level : can be “free” or “paid”
* page : Webpage visited, or button clicked, e.g. “NextSong”, “Thumbs Up”, “Logout”, “Downgrade”, …)
* method : HTTP Method “GET” or “POST”
* status : HTTP Response Code “200”, “307”, “404”
* userAgent : browser used, like “Mozilla/5.0 …(Win…) Firefox/31.0”
* sessionId : numeric session id for grouping session events
* itemInSession : number of this event in the user session
* auth : current status of authentication “Logged In”, “Logged Out“, …
* song : title of song, like “Time For Miracles”
* length : length of song in seconds with decimals “277.89016”
* artist : artist performing the song, like “Adam Lambert”

# Technologies
This project uses pyspark software

# Outcome
After exploring the datasets, here are the answers to our questions:

1- Extract the listings with the highest # of reviews (top 10). Which one got the highest % of positive reviews?

By exploring the data, we found that listing_id 815639 has the highest % of positive reviews (97.15%)

2- What are the top 3 most frequent neighbourhoods or zipcodes in Boston? (zipcodes with highest number of listings).

The highest zipcodes were ['02116', '02130', '02118']. We started by exploring the neighbourhood column, but it had around 15% missing values with no other source to impute the missing values, so we considered the zip code column

3- How the price correlates to the property_type? What types are the most expensive?

It was found that Guesthouse has the highest average price, but since we only had 1 record with this type, we moved to the next highest type which was "Boat"

# Resources
The columns description was obtained from https://medium.com/@ferenc.hechler/sparkify-customer-satisfaction-prediction-f3b0941e8710
