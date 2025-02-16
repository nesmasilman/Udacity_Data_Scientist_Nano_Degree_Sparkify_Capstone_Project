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

# Dataset
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
- We built three different machine learning models to predict churn (GBTClassifier, RandomForestClassifier, DecisionTreeClassifier). The one with the best performance was RandomForestClassifier, so we chose it for final prediction.
- We made three splits from the data (train, validation and test). We used the validation set for baseline model selection and Gridsearch cross-validation.
- We used gridseach cross-validation to try different parameters, but the best model didn't improve performance, so we used our baseline model.
- Our dataset is imbalanced, so we used f1-score to evaluate model performance. Best model scored 76.41% f1-score on our test set.
- We calculated feature importances. The two most important features were the average duration (avg number of subscription days) and the avg(length) which is the average length of songs.

# Resources
The columns description was obtained from https://medium.com/@ferenc.hechler/sparkify-customer-satisfaction-prediction-f3b0941e8710
