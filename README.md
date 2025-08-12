# Titanic_Classification_Project
Summer Class Final Project (2025) With Bhishan Poudel and Stempeers

**Class:** Summer Machine Learning Class 2025 (STEMPEERS)  
**Instructor:** Bhishan Poudel  
**Programmer:** Aditya Narayan 
**Date:** 2025-08-12

## Project Description
The goal of the project was to predict whether a passenger survived the Titanic crash by using machine learning models. We use historical data about passengers such as age, sex, class, fare, and cabin information to build models that can classify survival.

## Dataset
I used a Titanic dataset from Kaggle, created by M YASSER H, which contains information on passenger demographics, ticket class, fare, and survival outcome.

## Data Processing and Cleaning
1) I first converted non-numerical variables (`Sex`, `Embarked`, `Deck`) into numeric variables using mapping and one-hot encoding.
2) Next I filled missing values in `Age` with the mean age because the machine models cannot deal with empty values.
3) Third I extracted the deck from the cabin variable and cleaned the missing Cabin data.
4) Finally I split the data into training and testing sets (80%-20%).

## Models Used
1. Logistic Regression: Estimates the chance of survival by modeling the relationship between features and outcome using a curve that outputs probabilities between 0 and 1.
2. Decision Tree Classifier: Predicts survival by splitting the data into branches with yes/no rules based on feature values until a decision is made.
3. Random Forest Classifier: Builds many decision trees on random samples and combines their predictions to improve accuracy and reduce errors.

All models were trained on the training set and tested on the test set.

## Results
| Model               | Accuracy  |
|---------------------|-----------|
| Logistic Regression | 0.82      |
| Decision Tree       | 0.79      |
| Random Forest       | 0.79      |

Logistic Regression performed the best on the test set with an accuracy of 82%.

## Insights and Learnings
- I first did this without the class variable, however research showed that it was important and it also improved model accuracy. 
- I also toyed with the amount of iterations for the Logistic regression model and around 1000 gave the best results. 
- The Decision tree and random forest model showed very similar results. This is because between there predictions their was only 20 differences. 

## Next Steps
- Experiment with more advanced models or tuning hyperparameters.
- Explore additional features or use a new dataset with more information. 
- Use metrics beyond accuracy to evaluate model performance.

---
