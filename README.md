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
1. Logistic Regression:  Estimates the chance of survival by modeling the relationship between features and outcome using a curve that outputs probabilities between 0 and 1.
2. Decision Tree Classifier:  Predicts survival by splitting the data into branches with yes/no rules based on feature values until a decision is made.
3. Random Forest Classifier: Builds many decision trees on random samples and combines their predictions to improve accuracy and reduce overfitting.
4. Support Vector Machine (SVM): Finds the best boundary (hyperplane) to separate survivors from non-survivors, but can struggle without feature scaling or tuning.
5. K-Nearest Neighbors (KNN): Predicts survival based on how similar a passenger is to others nearby in the dataset. Sensitive to feature scaling and noisy data.
6. Naive Bayes: Uses probabilities and assumes all features are independent, which isn’t true for Titanic data but still gives decent performance.
7. AdaBoost Classifier: Builds several weak models (usually decision trees) in sequence, where each one focuses on the mistakes of the previous one.
8. Gradient Boosting Classifier:  Similar to AdaBoost but more powerful — builds trees gradually, each correcting the errors of the last to boost accuracy.

---

All models were trained on the training set and tested on the test set.

## Results
| Model                  | Accuracy |
|------------------------|----------|
| Logistic Regression    | 0.82     |
| Decision Tree          | 0.79     |
| Random Forest          | 0.79     |
| SVM                    | 0.66     |
| K-Nearest Neighbors    | 0.70     |
| Naive Bayes            | 0.79     |
| AdaBoost               | 0.80     |
| Gradient Boosting      | 0.81     |

Logistic Regression performed the best on the test set with an accuracy of 82%.

## Insights and Learnings
- Initially, I left out the passenger class (`Pclass`) feature, but adding it significantly improved accuracy across all models.
- I experimented with the number of iterations for Logistic Regression, and setting it to 1000 performed the best.
- Decision Tree and Random Forest gave nearly identical results because their predictions only differed on 20 passengers.
- Some models like SVM and KNN underperformed likely due to unscaled features — models sensitive to feature scale may need normalization.
- Ensemble models like Random Forest, AdaBoost, and Gradient Boosting were more accurate and robust compared to simpler models.

## Next Steps
- Experiment with more advanced models or tuning hyperparameters.
- Explore additional features or use a new dataset with more information. 
- Use metrics beyond accuracy to evaluate model performance.

---
