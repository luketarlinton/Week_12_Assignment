# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

* Within this anlaysis we used historical data from a peer to peer lending service of their lending activity. We aimed to build a model that could identify the creditworthiness of borrowers. This analysis evaluated models of imbalanced classes due to the fact that healthy loans greatly outweigh the number of risky loans.

* The data utilised within this analysis looked at historical data of lending activity using the following criterias; Loan size, interest rate, borrower income, debit to income, number of accounts, derogatory marks, total debt and finally loan status which indicated whether the loan was healthy or risky based on the before mentioned criteria.

* In termas of the variables we were trying to predict whether a loan was healthy (0) or risky (1) based on the data from the peer to peer lending service in which 75,036 loans were indicated as healthy and 2,500 were indicated as risky. 

* As part of this anyalsis we completed the following steps of the machine learining process; 
    * we split the data into labels and features sets, in which the Y variable was made up solely of the loan status criteria and the X variable was made up of all other crietria
    * we then split the data into training and testing sets
    * we then fit the training set to a logistic regression model and made predictions using this model and then finally evaluated the performance of the model
    * we then resampled the data using a random over sampler in an attempt to make the model more accurate given the imbalance between the healthy and risky loan numbers as healthy loans graetly outnumbered the risky loans. We the fit this resampled training data to a logistic regression model and made predictions using this model and then finally evaluated the performance of this model.



## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

    *The first logistic regression model was fairly accurate as dipected by the following results;
        * Balanced accuracy score: the model was 99.18% accurate. The balanced accuracy is the average of the recall scores of each class being healthy loans and risky loans.
        * Precision: The precision was 100% accuracte for positive predicitions for healthy loans and 85% accurate for risky loans.
        * Recall: The recall indicated 99% of positives were correctly identified for healthy loans and indicated 91% positives were correctly identified for risky loans

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

    *The second logistic regression model using the resampled data was more accurate as dipected by the following results;
        * Balanced accuracy score: the model was 99.47% accurate. The balanced accuracy is the average of the recall scores of each class being healthy loans and risky loans.
        * Precision: The precision was 99% accuracte for positive predicitions for healthy loans and 99% accurate for risky loans.
        * Recall: The recall indicated 99% of positives were correctly identified for healthy loans and indicated 99% positives were correctly identified for risky loans
        
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

* Machine Learning Model 2 (logistic regression model using the resampled data) performed the best out of the two models as it was the most accurate. This was indicated by the balanced accuracy score of 99.47% which was sligthly higher than the balanced accuracy score for Machine Learning Model 1. The reason for this increase in the balanced accuracy score was due to the higher recall that Model 2 had for the risky loans. This increase would be due to the oversampling that was used to counteract the imbalance between the number of healthy loans versus the risky loans as the number of healthy loans greatly outnumbers the risky.
* I would recommend Machine Learning Model 2 (logistic regression model using the resampled data) be used as it is more accurate than Machine Learning Model 1. It had a higher balanced accuracy score and had higher scores across both precision and recall (with the small exception of a slightly lower precision score for healthy loans than that of Machine Learning Model 1). It is more important to predict the scores of the 1's (risky loans) as the data used had a far smaller number of risky loans than that of healthy loans. It is also more important as that is what the model is being designed for. It is trying to predict whether a loan is risky as this is where the lender will face the greatest risks and what the lender wants to avoid.


