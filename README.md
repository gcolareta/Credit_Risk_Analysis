# Credit_Risk_Analysis

## Overview
In this project I am using machine learning to predict credit risk to determine if this approach will provide a quicker and more reliable loan experience. With the use of machine learning I am hoping to get more accurate predictions of low-risk candidates and decrease default loans.

## Results
Given that credit risk has an inherently classification problem, I performed a Logistic Regression using the oversampling techniques RandomOversampler and SMOTEN. Then, i used the undersampling technique ClusterCentriod algorithm to resample the dataset and compare which machine learning model gives me the most accurate prediction of credit risk.

I also used the SMOTEENN algorithm, which is a combination of the oversampling and undersampling techniques, to determine if the results are better at predicting credit risk than the resampling algorithms described above.

Finally, I performed a Balanced Random Forest Classifier and an Easy Ensembel Classifier to predict credit and evaluate each model.

When all the machine learning models were ran, they all produced the same value error in the same line of code: "*ValueError: could not convert string to float: 'f'*". These all happened when I was training the model using the resampled data. 

The first thing was to check that the features (X) and target variables (y) were converted from a string to a numeric value using an encoder, either get_dummies or the label encoder classifier.

I then turned to Google and try to find answers to my issue. I did try a few things, one of them including a function that would parse the large data with a different algorithm. All of these attempts were not successful. My guess is that the label encoder I used to convert the "y" values returned an int64 data type which was not supported by the model I was running. Unfortunately I do not have the knowledge to fix this with the information provided in the module and what I could learn from the internet.


## Summary
I am going to guess, based on the examples I learned in the module, that the imbalance in the classification (low-risk vs high-risk) was too pronounced. Low-risk counts were 68,470 compared to high-risk counts at 347
