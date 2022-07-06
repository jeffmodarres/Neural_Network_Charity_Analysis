# Module 19: Neural_Network_Charity_Analysis

## Overview
From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.
Goal is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results

* **Data Preprocessing**
    - **What variable(s) are considered the target(s) for your model?**
    There is column called "IS_SUCCESSFUL" which was used as target
    - **What variable(s) are considered to be the features for your model?**
    All other columns were considered as features. (few columns (EIN and NAME) were dropped due to not having any effect on the outcome)
    Features are variables that have impact on the outcome.
    - **What variable(s) are neither targets nor features, and should be removed from the input data?**
    Variables like EIN and NAME were dropped. These variable have no impact on the outcome 
* **Compiling, Training, and Evaluating the Model**
     - **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
     I used 3 layers  with 40 / 20/ 5 features. For hidden layers I used tahn activation function. For final output, sigmoid was used since we are classifying.  Layer params and functions were optimized to increase accuracy and reduce loss (training and testing loss).
     - **Were you able to achieve the target model performance?**
     I could only acheive training/testing loss of 74%/ 72% respectively.
    - **What steps did you take to try and increase model performance?**
    I used random forest to select important features. I also tried to play with learning rate but didn't see much benefit.
    I did change the activation functions and tanh/sigmoid perforemed better than the rest.

## Summary

using Random forest, I was able to acheive 70% accuracy in predicting target. When deep neural network was used, I could acheive 74% accuracy. 
I also used SVM and the result was comparable with other ML techniques. Finally I used AdaBoostClassifier and the result was 71%. 

In summary, neural network marginally outperfomed other techniques.

To furthur improve model performance, I think outliers must be filtered out. 