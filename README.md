# Credit_Risk_Analysis
## Overview
- The purpose of this analysis is to evaluate the performance of various machine learning models on datasets with unbalanced classes. Specifically, we will be looking at how effective the different machine learning models are at predicting whether or not a potential loan is risky. The models used will consist of oversampling, undersampling, and combination models. The final two models used are specifically tailored to reduce bias.

## Results
- The following images display the balanced accuracy scores as well as the classification reports that contain the precision and recall scores of each machine learning model

### Random Oversampling
![SupervisedML_Challenge_Screenshot_4](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/f27f88f7-0d95-4ce8-ad3f-7d0e485db882)
- Balanced Accuracy Score: 0.65 
- High Risk Precision Score: 0.01
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.62
- Low Risk Recall Score: 0.68
- Analysis: The Random Oversampling algorithm yields mediocre results with an accuracy of about 65%. This is mostly do to the fact that the High Risk Precision score is near 0, which is indicative of the model's inability to identify high risk loans. Specifically, the model is flagging low risk loans as high risk, thus driving down the model's high risk precision. However, the model is able to correctly predict whether or not a loan is low risk, with a perfect low risk precision score. Both of the Recall scores are mediocre with a slgihtly higher low risk recall score, indicating that the model is slightly better at finding low risk loans than high risk loans. 

### SMOTE Oversampling
![SupervisedML_Challenge_Screenshot_3](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/5e122471-505b-42d3-9fbd-137cb5e8f83b)
- Balanced Accuracy Score: 0.62
- High Risk Precision Score: 0.01
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.59
- Low Risk Recall Score: 0.66
- Analysis: The SMOTE algorithm yields very similar results to the Random Oversampling model, but actually performs slightly worse in nearly every category. This may suggest that reusing existing instances from the minority class in the model is actually better at predicting credit risk than creating synthetic instances to add to the underrepresented (high risk) class.

### Random Undersampling
![SupervisedML_Challenge_Screenshot_2](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/56985bc2-d48b-4f5f-b1e7-b123d042dd53)
- Balanced Accuracy Score: 0.59
- High Risk Precision Score: 0.01
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.61
- Low Risk Recall Score: 0.57
- Analysis: The Random Undersampling technique is perhaps the most underwhelming. With the lowest accuracy score and the lowest low risk recall score. It's clear that this model struggles to even identify all the low risk loans with a low risk recall score of just 0.57. 

### SMOTEENN(Combination Sampling) 
![SupervisedML_Challenge_Screenshot_1](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/ceb66ce0-9979-4b9a-b9da-227c4d137025)
- Balanced Accuracy Score: 0.65
- High Risk Precision Score: 0.01
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.71
- Low Risk Recall Score: 0.58
- Analysis: The combination sampling model is also unimpressive. The Random Oversampling model is just as accurate and actually has a higher low risk recall score. However, the high risk recall score is decent, meaning the combination model does okay when finding high risk loans. 

### Balanced Random Forest Classifier 
![SupervisedML_Challenge_Screenshot_5](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/3381f1f1-5332-44f2-aabe-fd529bff5264)
- Balanced Accuracy Score: 0.79
- High Risk Precision Score: 0.04
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.67
- Low Risk Recall Score: 0.91
- Analysis: Overall the ensemble algorithms perform much better than the other algorithms we've looked at thus far. The Balanced Random Forest Classifier, in particular, has an accuracy score of nearly 80% and is able to find over 90% of low risk loans. However, this model still underperforms when tasked with finding high risk loans and just like all the other models is unable to identify high risk loans with precision. 

### Easy Ensemble Adaboost Classifier 
![SupervisedML_Challenge_Screenshot_6](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/7c09ec6f-240c-454a-b6ec-4f832db2c5b3)
- Balanced Accuracy Score: 0.93
- High Risk Precision Score: 0.07
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.91
- Low Risk Recall Score: 0.94
- Analysis: The Easy Ensemble Adaboost Classifier is by far the best model, we've used, to analyze high and low risk credit loans. The model's accuracy is over 90% and both of it's recall scores are also above 90%. This means that regardless of the loan status, the model is proficient at identifying all of the loans requested. Unfortunately, the model is still unable to find only high risk loans, thus resulting in a high risk precision score of under 10%.

## Summary
- Based on the results gathered from our analysis, the Easy Ensemble Adaboost Classifier is far and away the best model that we used to analyze credit loan risk. As previously mentioned it vastly outperforms the other models in accuracy, high risk loan recall, and low risk loan recall (although the Balanced Random Forest Classifier performed well here too). It is also important to note that every model was able to avoid flagging a high risk loan as low risk which is indicated by the 1.00 low risk precision score that every model received. However, the all of the models struggled with finding high risk loans without mistakenly flagging low risk loans as high risk, with every model having a high risk precision score under 10%. Funny enough, when it comes to deciding which model, if any, can be used to reliably predict credit risk, the final verdict is ANY of the models will suffice. The reasoning behind this verdict is do to the nature of credit lending. The most important thing to consider is the goal of the lending company, which is to avoid high risk loans while giving out low risk loans, and while the Easy Ensemble Adaboost Classifier is better at the latter all of the models are perfectly capable of identifying only low risk loans, as indicated by the 100% low risk precision scores for all of the models. When tasked with flagging only low risk loans, every model was able to perform this task with 100% precision, which is ultimately the goal of the lending company, despite the models being unable to identify high risk loans without flagging low risk loans as high risk.
