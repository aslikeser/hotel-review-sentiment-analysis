# Customer Satisfaction Prediction through Hotel Review Analysis
This project centers on analyzing hotel reviews and stay details to predict customer satisfaction, providing actionable insights for Hotel Management Inc.     

We are tasked with helping Hotel Management Inc. better understand what qualities of a hotel stay contribute to greater customer satisfaction and higher ratings. For this analysis, you are provided with a large data set consisting of hotel reviews (text fields for positive and negative comments) and details about the stay (hotel location, time & length of stay, etc). Your target column of interest is __Reviewer_Score__ which encodes positive sentiment as 1 and negative as 0.

You can download the data set from [here](https://api.brainstation.io/content/link/1qEa80Su0jdmJ8GK0bGr0aaYUZoaWAKvO).

You will begin with some Exploratory Data Analysis (EDA), and then move into data processing, modeling, and iteration over model improvements.

## Exploratory Data Analysis
First, load the data and understand what we are working with.

Perform EDA on the data and mention 3-4 observations from which you can draw actionable insights. In your EDA, you may consider creating a data dictionary, basic statistical analysis, data visualizations, data cleaning, and preprocessing to prepare the data for modeling.

## Preprocessing
Next, the text data needs to be processed for modeling.

Split the data into train and test sets and transform the positive and negative review columns using a CountVectorizer. 

Consider the following:
- What tokenizer and text cleaning steps do you include?   
- Using the vectorizer, maximize the number of features at 500 and make sure that tokens used <10 times are dropped from the vocabulary.
- This process may be done on the positive and negative review columns separately and then the resulting arrays merged with the original numeric features to form the final train and test data frames ready for modeling.
- In your column names, make sure you mark which words are coming from the positive vs negative reviews (you can use a prefix such as pos_ and neg_).

## Modelling
As the data is now ready for modeling, we will be creating two separate models with optimization and evaluation of each.

- Fit a logistic regression model on the data and analyze the test and train accuracy. Find the top 20 words from the positive reviews that are most predictive of a positive sentiment (Reviewer_Score = 1). Similarly, find the top 20 words from the negative reviews that are most predictive of negative sentiment (Reviewer_Score = 0). What actionable insights can you draw from these?

- Using a pipeline, combine PCA with a decision tree classifier.
  - Optimize at least 3 hyperparameters including the maximum tree depth and the minimum number of data points required on each leaf node.
  - You can use 20 principle components.
  - The best parameters should be found using 5-fold cross-validation.
  - Contrast the best results here with the logistic regression model and provide any insights that you may draw from the results.

- For your best-performing model, conduct a more in-depth evaluation by analyzing the confusion matrix and commenting on the model errors and metrics such as precision and recall.
