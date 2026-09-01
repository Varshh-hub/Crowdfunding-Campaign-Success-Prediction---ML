# Crowdfunding Campaign Success Prediction

## Project Overview

This project focuses on predicting whether a crowdfunding campaign will be **Successful** or **Unsuccessful** using machine learning classification algorithms.

Crowdfunding platforms host campaigns across different categories such as technology, education, healthcare, and creative arts. The success of a campaign can depend on factors such as funding goals, campaign duration, backer engagement, and pledged amounts.

The objective of this project is to build, evaluate, compare, and tune multiple classification models to determine which machine learning algorithm performs best at predicting crowdfunding campaign outcomes.

---

#  Classification Models

Five classification algorithms were implemented and compared.

## 1. Random Forest Classifier

Random Forest uses multiple decision trees and combines their predictions to improve classification performance and reduce individual tree overfitting.

## 2. K-Nearest Neighbors (KNN)

KNN classifies a new observation based on the classes of its nearest neighboring observations.

## 3. Decision Tree

Decision Tree uses a series of decision rules to divide the data and classify campaigns into successful or unsuccessful categories.

## 4. Naive Bayes

Naive Bayes is a probabilistic classification algorithm based on Bayes' theorem.

## 5. Support Vector Machine (SVM)

A linear Support Vector Machine was used to efficiently classify the large crowdfunding dataset.

---
# 📈 Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

#  Final Model Results

The following results were obtained after training and evaluating the classification models.

| Model         | Train Accuracy | Test Accuracy |    Precision |       Recall |     F1-Score |
| ------------- | -------------: | ------------: | -----------: | -----------: | -----------: |
| **SVM**       |   **99.9313%** |  **99.9300%** | **99.9501%** | **99.9102%** | **99.9301%** |
| Decision Tree |       99.8650% |      99.2400% |     99.3103% |     99.1716% |     99.2409% |
| Random Forest |       99.7513% |      91.1600% |     98.4612% |     83.6610% |     90.4597% |
| KNN           |      100.0000% |      69.7250% |     70.7539% |     67.4419% |     69.0582% |
| Naive Bayes   |       66.3600% |      66.8250% |     73.9932% |     52.0810% |     61.1329% |

---

#  Best Performing Model

Based on the evaluation results, the **Support Vector Machine (SVM)** achieved the best overall performance.

## SVM Performance

| Metric            |        Score |
| ----------------- | -----------: |
| Training Accuracy | **99.9313%** |
| Testing Accuracy  | **99.9300%** |
| Precision         | **99.9501%** |
| Recall            | **99.9102%** |
| F1-Score          | **99.9301%** |

The extremely small difference between training and testing accuracy indicates that the SVM generalized very well to the unseen test data.

The SVM achieved the highest F1-score among all evaluated models and was therefore selected as the final model.

---

# 📊 Model Performance Analysis

## SVM

SVM produced the strongest overall performance, achieving approximately **99.93% test accuracy** and **99.93% F1-score**.

Its training and testing performance were almost identical, indicating strong generalization.

The test precision of **99.95%** and recall of **99.91%** also demonstrate that the model was highly effective at distinguishing successful and unsuccessful campaigns.

---

## Decision Tree

The Decision Tree achieved approximately **99.24% test accuracy** and **99.24% F1-score**.

Its training accuracy was **99.865%**, while its testing accuracy was **99.24%**.

Although there is a small difference between training and testing performance, the model still demonstrated strong predictive performance.

Decision Tree was the **second-best-performing model** in the final comparison.

---

## Random Forest

Random Forest achieved a training accuracy of approximately **99.75%**, but its test accuracy decreased to approximately **91.16%**.

The model achieved:

* Precision: **98.46%**
* Recall: **83.66%**
* F1-score: **90.46%**

The noticeable difference between training and testing performance suggests that the model may be overfitting the training data.

The relatively high precision combined with lower recall indicates that although Random Forest was effective when predicting successful campaigns, it missed a noticeable number of actual successful campaigns.

---

## KNN

KNN achieved **100% training accuracy**, but its test accuracy was only approximately **69.73%**.

The model achieved:

* Precision: **70.75%**
* Recall: **67.44%**
* F1-score: **69.06%**

The large difference between training and testing performance indicates significant overfitting.

This suggests that although KNN was able to perfectly classify the training observations, it did not generalize effectively to unseen campaigns.

---

## Naive Bayes

Naive Bayes produced the lowest overall performance among the five models.

It achieved:

* Training Accuracy: **66.36%**
* Test Accuracy: **66.83%**
* Precision: **73.99%**
* Recall: **52.08%**
* F1-score: **61.13%**

The relatively low recall indicates that the model failed to identify a significant proportion of successful campaigns.

---

#  Hyperparameter Tuning

Hyperparameter tuning was performed using `RandomizedSearchCV`.

`RandomizedSearchCV` was selected instead of exhaustive `GridSearchCV` to reduce computational cost while still exploring different hyperparameter combinations.

The models were tuned using selected parameters such as:

* Number of estimators
* Maximum tree depth
* Minimum samples split
* Number of neighbors
* Distance metric
* Decision tree criterion
* Naive Bayes smoothing
* SVM regularization parameter `C`

The best parameter combination was selected using the F1-score from cross-validation.

---

# Final Model Comparison Summary

| Rank | Model             | Test Accuracy |   F1-Score | Observation                |
| ---: | ----------------- | ------------: | ---------: | -------------------------- |
|    1 | **SVM**           |    **99.93%** | **99.93%** | Best overall performance   |
|    2 | **Decision Tree** |    **99.24%** | **99.24%** | Strong performance         |
|    3 | **Random Forest** |    **91.16%** | **90.46%** | Noticeable train-test gap  |
|    4 | **KNN**           |    **69.73%** | **69.06%** | Significant overfitting    |
|    5 | **Naive Bayes**   |    **66.83%** | **61.13%** | Lowest overall performance |
---

#  Conclusion

This project successfully implemented a complete machine learning classification workflow for predicting crowdfunding campaign success.

Five classification algorithms — **Random Forest, KNN, Decision Tree, Naive Bayes, and SVM** — were trained and evaluated using Accuracy, Precision, Recall, F1-score, and Confusion Matrix.

Cross-validation was used to evaluate model stability, while `RandomizedSearchCV` was used for hyperparameter tuning.

Among all the models, **SVM achieved the best performance**, with a **99.93% testing accuracy** and **99.93% F1-score**. Its training accuracy of **99.93%** was also extremely close to its testing accuracy, suggesting strong generalization to unseen data.

The **Decision Tree** was the second-best-performing model, achieving **99.24% test accuracy** and **99.24% F1-score**.

**Random Forest** achieved strong performance but showed a noticeable difference between training and testing results, while **KNN** demonstrated significant overfitting with 100% training accuracy but only 69.73% test accuracy.

**Naive Bayes** produced the lowest overall performance, with 66.83% test accuracy and a 61.13% F1-score.

Overall, the project demonstrates the complete process of building, validating, tuning, comparing, and selecting a machine learning classification model for a real-world prediction problem.

---

# 👩‍💻 Author

**Varsha A**

**B.Sc. Artificial Intelligence & Machine Learning**

**Data Science & Machine Learning Project**
