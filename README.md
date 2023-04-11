# CREDIT CARD FRAUD DETECTION
![image](https://user-images.githubusercontent.com/116062465/231133305-0696d3b3-ce64-4c0e-b1df-afb357abc931.png)

# Overview  
Credit card fraud is defined as a fraudulent transaction (payment) that is made using a credit or debit card by an unauthorized user.Credit cards are now the most preferred way for customers to transact either offline or online, due to the advancement in communication and electronic commerce systems.It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase.  

# Business understanding  
Fraud associated with transactions has increased significantly and fraud detection has become a challenging task because of the constantly changing nature and patterns of the fraudulent transactions.This has sparked the proliferation and increase in the use of services such as e-commerce, tap and pay systems, online bills payment systems etc. As a consequence, fraudsters have also increased activities to attack transactions that are made using credit cards.It is therefore crucial to implement effective and efficient mechanisms that can detect credit card fraud to protect users from financial loss.  

## Main objective  
Due to the increase in fraudulent activities it has become essential for financial institutions and businesses to develop advanced fraud detection techniques to counter the threat of fraudulent credit card transactions and identity theft and keep losses to a minimum  

# Data understanding  
The dataset used for this project was acquired from [Kaggle](https://www.kaggle.com/datasets/kartik2112/fraud-detection?select=fraudTest.csv) . This dataset contains financial transactions that have been simulated using a real-world financial transactions dataset and it has 23 columns and rows. The target variable(is fraud) which is a binary indicator shows that whether the transaction is fraudulent 1 or not 0.We performed an exploratory data analysis to the training data to understand which features were correlated to fraudulent activities and then attempted to create models with those features and test out their predicitve effectiveness.The dataset contained the folowing features.  

# Data Pre Processing  
The columns were renamed to a proper and understandable way,checked for features that have high correlation with the target(Is Fraud) variable and the irrelevant columns dropped.Categorical columns were Label encoded and the numerical columns were scaled using MinMaxScaler() so that all features got to the same scale improving the model performance.Since we had less cases of fraud in our dataset we used **SMOTE** to balance the dataset sto increase the representation of the minority class in the training data.  

# Modelling  
In coming up with the best model, the following approach will be taken:
- We ran different classification models i.e Logistic Regression,Random Forest, Decision Tree  and K Nearest Neighbors on the balanced training dataset.
- Of the four classifiers,Random Forest and Decision Tree were the top best and were selected for  Hyperparameters tuning  ( taking into account prediction accuracy and recall).

# Evaluation  
A randomforest classifier and Decision Tree were chosen as the two best models and compared against each other according to their performance on predicting new unseen data. in line with the business problem. The Decision Tree model was chosen as the model for deployment as it had an ROC of  98% and a recall of 90%.

# Conclusions
- The number of fraud transactions are very few compared to legitimate transactions and it has to be balanced in order for a fair comparison to prevent the model from overfitting.
- From the data females and males are almost equally susceptible (50%) to transaction fraud. 
- Most fraudulent activities occur from 10pm,and this is when most people are asleep.

# Recommendations  
- For every transaction that is flagged as fraudulent, we can add the human element to verify whether the transaction was done by calling the customer. However, when precision is low, such tasks are a burden because the human element has to be increased.
- For banks having a larger transaction value, if the recall is low, i.e., it is unable to detect transactions that are labelled as non-fraudulent. So we have to consider the losses if the missed transaction was a high-value fraudulent one.
- For banks with smaller average transaction value, we would want high precision because we only want to label relevant transactions as fraudulent.
- So here, to save the banks from high-value fraudulent transactions, we have to focus on a high recall in order to detect actual fraudulent transactions.


# Repository guide
- The data set used can be found [here](https://www.kaggle.com/datasets/kartik2112/fraud-detection?select=fraudTest.csv)
- The data report can be found [here]
- The notebook can be found [here]
- The Presentation Slides can be found [here]


