# Supervised-Learning-Challenge
My main objective of this task was to build a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not.

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

I had to use this data to create machine learning models to classify the risk level of given loans. Specifically, I had to compare the Logistic Regression model and Random Forest Classifier.

An entire year's worth of data (2019) from LendingClub was used to predict the credit risk of loans from the first quarter of the next year (2020). The two CSVs being used have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.

# Preprocessing: Convert categorical data to numeric
A training set from the 2019 loans was created using label encoding to convert the categorical data to numeric columns. 

<img width="859" alt="2022-09-04" src="https://user-images.githubusercontent.com/92040392/188330692-ac071e2d-6127-436a-b76c-596158ec6189.png">

The same method was used to create a testing set from the 2020 loans with the addition of pd.get_dummies(), a one-hot encoding method of data preprocessing.

<img width="865" alt="2022-09-04 (1)" src="https://user-images.githubusercontent.com/92040392/188330829-118013ff-6e8e-428a-8f3c-8631247e938e.png">

Before I created, fitted, and scored the models, my prediction was that the random forest classifier will fit the data better than logistic regression, however when scaled, the latter will outperform it.

# Logistic Regression

<img width="868" alt="2022-09-04 (2)" src="https://user-images.githubusercontent.com/92040392/188331298-1835485e-0c0c-4a16-ad02-3ba03cf044d7.png">

# Random Forest Classifier

<img width="863" alt="2022-09-04 (3)" src="https://user-images.githubusercontent.com/92040392/188331417-80493044-a2c5-4daf-8cff-e96e62d3998b.png">

# Scaled Data
Logistic Regression:

<img width="880" alt="2022-09-04 (4)" src="https://user-images.githubusercontent.com/92040392/188331544-c01cdb50-6689-4f3b-9e4b-2754a8314ddd.png">

Random Forest Classifier:

<img width="864" alt="2022-09-04 (5)" src="https://user-images.githubusercontent.com/92040392/188331600-cefa6b1f-268d-4bcc-8c19-949a3f337d63.png">

Reference:

LendingClub (2019-2020) Loan Stats. Retrieved from: https://resources.lendingclub.com/
