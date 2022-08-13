# Credit_Risk_Analysis

## Analysis Overview

### Problem Statement: 
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. 

### Methodology: 
For this challenge, I employed different techniques to train and evaluate models with unbalanced classes. I used the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. 

Lastly, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Below, you’ll see my evaluation of the performance of these models and my recommendation on whether they should be used to predict credit risk.

- - - -

## Machine Learning Algorithms Used

1. RandomOverSampler
2. SMOTE
3. ClusterCentroids
4. SMOTEENN
5. BalancedRandomForestClassifier
6. EasyEnsembleClassifier

- - - -

## Results

### RandomOverSampler

* Balanced accuracy Score: 0.655
* Precision Score: high risk  = 0.01  low risk = 1
* Recall Scores: high risk  = 0.72  low risk = 0.59

<img width="1027" alt="ROS Accuracy Score" src="https://user-images.githubusercontent.com/103781847/184501121-0c5b6a53-77d6-4b05-be87-1fe02a345b7a.png">

<img width="1019" alt="ROS Classification report" src="https://user-images.githubusercontent.com/103781847/184501128-7016739b-878c-432d-8b25-8ff6879ae2ac.png">

### SMOTE

* Balanced accuracy Score: 0.662
* Precision Score: high risk  = 0.01  low risk = 1
* Recall Scores: high risk  =0.63 low risk = 0.69

<img width="1015" alt="SMOTE Oversampling Accuracy Score" src="https://user-images.githubusercontent.com/103781847/184501165-39d007e2-ee60-4df4-928a-2f4a43a218ab.png">

<img width="1024" alt="SMOTE Oversampling Classification Report" src="https://user-images.githubusercontent.com/103781847/184501170-c5b9571a-1072-4b59-b3d2-0bf62f3c6911.png">

### ClusterCentroids

* Balanced accuracy Score: 0.662
* Precision Score: high risk  = 0.01  low risk = 1
* Recall Scores: high risk  = 0.69  low risk = 0.40

<img width="1020" alt="ClusterCentroids Accuracy Score" src="https://user-images.githubusercontent.com/103781847/184501179-199ba8a8-f175-493e-97f5-b3f7fcf78a44.png">

<img width="1025" alt="ClusterCentroids Classification Report" src="https://user-images.githubusercontent.com/103781847/184501186-11530354-6538-4465-88c8-cdf0f95c3809.png">

### SMOTEENN

* Balanced accuracy Score: 0.544
* Precision Score:high risk  = 0.01  low risk = 1
* Recall Scores: high risk  = 0.72  low risk = 0.61

<img width="1025" alt="Smoteen Accuracy Score" src="https://user-images.githubusercontent.com/103781847/184501204-de8f34d0-7d2d-431b-b942-eb01825de28f.png">

<img width="1013" alt="Smoteen Classification Report" src="https://user-images.githubusercontent.com/103781847/184501208-12a5f47c-0b9b-4f93-ba28-e9d27938ed70.png">

### BalancedRandomForestClassifier

* Balanced accuracy Score: 0.789
* Precision Score: high risk  = 0.03  low risk = 1
* Recall Scores: high risk  = 0.70  low risk = 0.87

<img width="1023" alt="BRF Accuracy Score" src="https://user-images.githubusercontent.com/103781847/184501217-63f14de2-4459-4380-9ee9-649ecb53abba.png">

<img width="1016" alt="BRF Classification Report" src="https://user-images.githubusercontent.com/103781847/184501225-ff729d6e-241b-4530-b7ae-2cd2a322602d.png">

### EasyEnsembleClassifier

* Balanced accuracy Score: 0.931
* Precision Score: high risk  = 0.09  low risk = 1
* Recall Scores: high risk  = 0.92  low risk = 0.94

<img width="1019" alt="EEC Accuracy Score" src="https://user-images.githubusercontent.com/103781847/184501234-6334bfd5-7073-43c2-a2e0-ff7b75028cdd.png">

<img width="1020" alt="EEC Classification Report" src="https://user-images.githubusercontent.com/103781847/184501239-ec9ed228-55d4-4271-9f99-eb7e09e38c17.png">

- - - -

## Summary of the model results + recommendations

Of the six different algorithms we tested, the first 4 did not perform as well as the last two. The Easy Ensemble model performed the best, by far. I would recommend using the Easy Ensemble algorithm if they are choosing from the 6 we tested. That being said, it would be helpful to understand the baseline/goal accuracy, precision and recall scores that the bank is targeting as a minimum viable product. 

Something else for them to consider would be their appetite for using a mix of machine learning and manual reviews. They could use machine learning to weed out the applications that are most clearly high/low risk and have the more middle-ground applications get reviewed by a manual review team if they want to absolutely reduce business risk and client insult. 
