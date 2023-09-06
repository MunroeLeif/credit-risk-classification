# Credit Risk Analysis Report

## Overview of the Analysis

The purpose of this analysis was to assess historic loan data in order to create a model capable of predicting the creditworthyness of potential borrowers. The data contains details of historic loans such as loan size, interest rate, the borrowers debt to income ratio, and importantly the status of the loan(`0`: healthy loan, `1`: high-risk loan). The model was trained to predict the likely status of prospective borrowers using a logistic regression model. Because the data was heavily skewed in favor of healthy loan data points, the data was resampled using the Random Oversampler module from the imbalance-learn library in order to see the balanced results as well. 

## Results

* Model 1: Original data
    * Accuracy: The model has good overall accuracy of 0.957
    * Precision: With a precision score of `0`= 100% compared with `1`= 85% we can see that the weakness of this model lies in the heavily unbalanced number of healthy loans to high-risk loans, which results in a much diminished precision for `1` predictions
    * Recall: The recall values of `0`= 99% and `1`= 92% reflect the unbalanced precision scores, with `0` returning much higher percentage

* Model 2: Resampled data
    * Accuracy: The second model as a great overall accuracy of 0.995
    * Precision: The precision scores of `0`= 99% and `1`= 99% reflect the now-balanced data set, with the same number of inputs resulting in the same precision for both loan categories
    * Recall: The recall scores of `0`= 99% and `1`= 99% reflect the same balance in the data set

## Summary 

Based on the evaluation of the models' performance (using accuracy, precision and recall values), the 2nd Model made with resampled data preforms overall best. Because it is doing the analysis with the same number of inputs for both categories, it is able to predict the likely value of a loan's status with greater overall accuracy. 
Given the nature of this loan information, predicting potential defaulters (`1`) is likely more important to lenders assessing potential borrowers. For this reason, as well as it's higher overall accuracy, I would recomend that the company employ Model 2. 
