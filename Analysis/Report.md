Report Template

## Overview of the Analysis

The purpose of the analysis was to create a logistic regression model, with the intent to predict accurately whether or not we can label the data into two categories; high-risk loans and healthy loans. The data included 7 different variables e.g. loan size, interest rate etcwhich constituted the X variables.There was only one outcome variable, whether the loan is healthy (0) or at high-risk (1), which became the y variable. When initially analysing the original data set, the loan_status outcome was imbalanced, with a high number of healthy loans, 75036, compared to only 2500 high-risk loans. Therefore, we first performed a logitstic regression ananlysis on the imbalanced original data set by splitting up the data into training and test sets. The analysis was then performed again, but this time the dataset was resampled via oversampling. This allowed the oversampled data set to have exact equal amounts of healthy loans and at-risk loans in the dataset, which would allow for a different outcome on the accuracy, precision and recall of the model.

## Results

# * Machine Learning Model 1 (Orignal Dataset):
 
  * Accuracy: 99%, although a very imbalanced dataset, with very high number of healthy-loans compared to high-risk loans. Does not mean much by itself.

  * Precision: 100% for healthy loans, to be expected as the healthy loans are the majority of the dataset. 87% for high-risk loans, therefore quite well at predicting the true postitive calls of at-risk loans (low false positives).

  * Recall: Again 100% for healthy loans. 89% for high-risk loans, so the model does well at predicting a low amount of false negatives.


# * Machine Learning Model 2 (Oversampled Dataset):
  
  * Accuracy: 100%, although we know from the confusion matrix, that there were a total of 93 false positives/negatives so not entirely 100% accurate but close enough.

  * Precision: 100% for healthy loans, therefore model is doing well at predicting true positives for these types of loans. Precision is the same as the original data set for high-risk loans, 87%, so the model is doing well at predicting true positive calls of these loans.

  * Recall: Again 100% for healthy loans. Although now for high-risk loans, the recall is at 100% with only 2 false negatives predicted in the entire data set, which is much improved compared to the original dataset.

## Summary

Overall, both machine learning models performed well with >85% scores in the 3 categories used above. The resampled via oversampling machine learning model provided a better model due to the fact that the recall was significantly improved. For this problem it is better to accurately predict the high-risk loans (1), rather than the healthy loans as these are more detrimental to the company. Therefore, false negatives are more costly as the company would not want high-risk loans to be categorized as healthy and the model with the highest recall should be used to predict as least as possible false negatives. The logisitic regression model utilizing oversampling should be used to predict these loans for due to this reasoning.


