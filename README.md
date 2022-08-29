# Email-Classification
### Objective: Classify emails into 6 different categories based on the content of the emails.
Data taken for the model is labeled email data. Emails belonging to same class are in same folder containing each email in txt format. 1663 emails are extracted from 6 folders. Each class is mapped from 0 to 5.
From each email its subject and body is extracted using two functions with the help of email library. The email classifier focuses on subject and body of the email only.
## Data is imbalanced
### Feature representation: Bag of Words and TFIDF.
### Models used: 
 Naive Bayes: Works well with text data 
 Random Forest: Better with imbalanced dataset 
 XGBoost: Boosting technique to increase the performance 
 SVM: Works good with large number of features
## Solving Imbalanced Dataset Problem
### Use of cost-sensitive Random Forest: 
Made Random Forest Classifier bias towards those classes that have fewer examples in the training dataset. No significant improvement in the performance.
### Use of Text Augmentation Technique to increase data size of minority classes:
Used nlpaug library to artificially increase training data size of minority group by generating different versions of real datasets without actually collecting the data.
#### Significant Improvement in F1- score from 0.36 to 0.80
### Use of resampling technique:
Resampling method is a tool consisting in repeatedly drawing samples from a dataset. It increased number of minority class to 400.
Significant Improvement in F1 score from 0.36 to 0.91.
## Result: Using text augmentation technique and over resampling technique. Performance of Naïve Bayes and Random Forest model significantly increased.

