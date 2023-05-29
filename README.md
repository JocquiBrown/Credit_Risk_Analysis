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
- Analysis: 

### SMOTE Oversampling
![SupervisedML_Challenge_Screenshot_3](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/5e122471-505b-42d3-9fbd-137cb5e8f83b)
- Balanced Accuracy Score: 0.62
- High Risk Precision Score: 0.01
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.59
- Low Risk Recall Score: 0.66
- Analysis: 

### Random Undersampling
![SupervisedML_Challenge_Screenshot_2](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/56985bc2-d48b-4f5f-b1e7-b123d042dd53)
- Balanced Accuracy Score: 0.59
- High Risk Precision Score: 0.01
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.61
- Low Risk Recall Score: 0.57
- Analysis: 

### SMOTEENN(Combination Sampling) 
![SupervisedML_Challenge_Screenshot_1](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/ceb66ce0-9979-4b9a-b9da-227c4d137025)
- Balanced Accuracy Score: 0.65
- High Risk Precision Score: 0.01
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.71
- Low Risk Recall Score: 0.58
- Analysis: 

### Balanced Random Forest Classifier 
![SupervisedML_Challenge_Screenshot_5](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/3381f1f1-5332-44f2-aabe-fd529bff5264)
- Balanced Accuracy Score: 0.79
- High Risk Precision Score: 0.04
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.67
- Low Risk Recall Score: 0.91
- Analysis: 

### Easy Ensemble Adaboost Classifier 
![SupervisedML_Challenge_Screenshot_6](https://github.com/JocquiBrown/Credit_Risk_Analysis/assets/120291854/7c09ec6f-240c-454a-b6ec-4f832db2c5b3)
- Balanced Accuracy Score: 0.93
- High Risk Precision Score: 0.07
- Low Risk Precision Score: 1.00
- High Risk Recall Score: 0.91
- Low Risk Recall Score: 0.94
- Analysis: 

## Summary
- Based on the results gathered from our analysis, 
