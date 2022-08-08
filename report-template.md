# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

out of everytime we predicted the false positives and true positives, how many were actually correct?
precision compares predicted true values, how often were they correct. Precision shows false positives.
TP divided by TP PLUS FP

recall is the ratio between true positives and false negatives. focus being on how often are we giving a negative to a positive. higher recall means the model may sacrifice some precision, but reduces false negatives.
recall high means low false negatives.
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
Using a Logistic Regression Model with the original data, we attained an accuracy score of .95, indicating the average recall
of our obtained class had a low amount of false negatives. With a precision of 1 in our healthy loans and .85 in our high risk loans, we found that the more reliably accurate class was the healthy loan model. It also contained the highest recall, .99 against the high-risk models .91. The confusion matrix indicated that out of nearly 20000 predictions only 102 were false positive and 56 were false negative, though not perfect, this is representive of our high recall scores particularly in the healthy loans model.


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
Using the Logistic Regression Model on our resampled training data means we can utilise our predicted data to effectually gain more accurate recall and accuracy returns. However in my tests results were very similar, however both the recall consitently came to .99, higher than than the original data. There was a slight increase to false negatives (116 to 102) but false negatives returned 4 to 56, indicating the recall being slightly more effective agains the original data model.
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Either Logistic Model could be used, however due to its less complicated and more accurate nature, using the orginal data model it is easier to to train and test data on aswell as function with minimal reason for doubt as we train against original data and not predictions. The healthy loan model also produced a higher recall rate over both the original and random over sampled model data, meaning that false negatives were reduced. Both models produced a '1' accuracy score with the healthy loans class. Indicating that it minimised false positives, which is most important because innacurately identifying a loan approval to a high risk customer could result on a default that was approved due to a failure by the machine learning algorithm.
