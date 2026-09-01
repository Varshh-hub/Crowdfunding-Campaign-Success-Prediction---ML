# Crowdfunding Campaign Success Prediction

## Project Overview

This project focuses on predicting whether a crowdfunding campaign will be **Successful** or **Unsuccessful** using machine learning classification algorithms.

Crowdfunding platforms host campaigns across different categories such as technology, education, healthcare, and creative arts. The success of a campaign can depend on factors such as funding goals, campaign duration, backer engagement, and pledged amounts.

The objective of this project is to build, evaluate, compare, and tune multiple classification models to determine which machine learning algorithm performs best at predicting crowdfunding campaign outcomes.

---
## 📊 Dataset

The project uses the **Crowdfunding Campaign Dataset** provided for the Data Scientist Module 4 Assignment 07.

### Dataset Details

| Property          | Value                         |
| ----------------- | ----------------------------- |
| Dataset           | Crowdfunding Campaign Dataset |
| Number of Records | 100,000                       |
| Number of Columns | 14                            |
| Target Variable   | `IsSuccessful`                |
| Identifier Column | `CampaignID`                  |

### Target Variable

The target variable `IsSuccessful` represents the outcome of a crowdfunding campaign.

| Value | Meaning      |
| ----- | ------------ |
| `0`   | Unsuccessful |
| `1`   | Successful   |

The target classes are approximately balanced, allowing the models to be trained without applying an additional class-balancing technique.

---

## 🤖 Classification Models

Five classification algorithms were implemented and compared.

### 1. Random Forest Classifier

Random Forest uses multiple decision trees and combines their predictions to improve classification performance and reduce individual tree overfitting.

### 2. K-Nearest Neighbors (KNN)

KNN classifies a new observation based on the classes of its nearest neighboring observations.

### 3. Decision Tree

Decision Tree uses a series of decision rules to divide the data and classify campaigns into successful or unsuccessful categories.

### 4. Naive Bayes

Naive Bayes is a probabilistic classification algorithm based on Bayes' theorem.

### 5. Support Vector Machine (SVM)

A linear Support Vector Machine was used to efficiently classify the large crowdfunding dataset.

---

## 📈 Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## 🏆 Final Model Results

The following results were obtained after training and evaluating the classification models:

| Model         | Train Accuracy | Test Accuracy |    Precision |       Recall |     F1-Score |
| ------------- | -------------: | ------------: | -----------: | -----------: | -----------: |
| **SVM**       |   **99.9313%** |  **99.9300%** | **99.9501%** | **99.9102%** | **99.9301%** |
| Decision Tree |       99.8650% |      99.2400% |     99.3103% |     99.1716% |     99.2409% |
| Random Forest |       99.7513% |      91.1600% |     98.4612% |     83.6610% |     90.4597% |
| KNN           |      100.0000% |      69.7250% |     70.7539% |     67.4419% |     69.0582% |
| Naive Bayes   |       66.3600% |      66.8250% |     73.9932% |     52.0810% |     61.1329% |

---

## 🥇 Best Performing Model

Based on the evaluation results, the **Support Vector Machine (SVM)** achieved the best overall performance.

---

## 📊 Model Performance Analysis

### SVM

SVM produced the strongest overall performance, achieving approximately **99.93% test accuracy** and **99.93% F1-score**.

Its training and testing performance were almost identical, indicating strong generalization.

### Decision Tree

Decision Tree also performed very well, achieving approximately **99.24% test accuracy**.

However, its performance was slightly lower than SVM.

### Random Forest

Random Forest achieved a very high training accuracy of approximately **99.75%**, but its test accuracy dropped to approximately **91.16%**.

This indicates a noticeable difference between training and testing performance.

### KNN

KNN achieved **100% training accuracy**, but its test accuracy was only approximately **69.73%**.

This large performance gap indicates significant overfitting.

### Naive Bayes

Naive Bayes produced the lowest overall performance, with approximately **66.83% test accuracy** and **61.13% F1-score**.

---

## ⚙️ Hyperparameter Tuning

Hyperparameter tuning was performed using **RandomizedSearchCV**.

RandomizedSearchCV was selected instead of exhaustive GridSearchCV to reduce computational cost while still exploring different hyperparameter combinations.

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

## 🧠 Why F1-Score Was Used

F1-score was used as an important metric for model comparison because it considers both **precision and recall**.

This is useful when evaluating whether campaigns are correctly classified as successful or unsuccessful.

The final model was selected by considering:

* Test accuracy
* Precision
* Recall
* F1-score
* Cross-validation performance
* Difference between training and testing performance

---

## 📌 Model Comparison Summary

| Rank | Model         | Test Accuracy |   F1-Score | Observation                      |
| ---: | ------------- | ------------: | ---------: | -------------------------------- |
| 🥇 1 | SVM           |    **99.93%** | **99.93%** | Best overall performance         |
| 🥈 2 | Decision Tree |    **99.24%** | **99.24%** | Strong performance               |
| 🥉 3 | Random Forest |        91.16% |     90.46% | Training performance much higher |
|    4 | KNN           |        69.73% |     69.06% | Significant overfitting          |
|    5 | Naive Bayes   |        66.83% |     61.13% | Lowest overall performance       |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Jupyter Notebook / Google Colab**

---

## 📁 Project Structure

```text
Crowdfunding-Campaign-Success-Prediction/
│
├── data.csv
├── model.ipynb
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib scikit-learn
```

### 3. Add the Dataset

Place the dataset in the project directory:

```text
data.csv
```

### 4. Open the Notebook

Using Jupyter:

```bash
jupyter notebook
```

Alternatively, upload the notebook to Google Colab.

### 5. Run the Notebook

Execute the notebook cells sequentially to perform:

1. Data exploration
2. Data preprocessing
3. Feature selection
4. Train-test splitting
5. Model training
6. Model evaluation
7. Cross-validation
8. Hyperparameter tuning
9. Model comparison
10. Final model selection

---

## 📚 Key Learning Outcomes

This project provided practical experience in:

* Data cleaning
* Exploratory data analysis
* Feature selection
* Categorical encoding
* Feature scaling
* Classification algorithms
* Train-test splitting
* Model evaluation
* Confusion matrices
* Cross-validation
* Hyperparameter tuning
* RandomizedSearchCV
* Model comparison
* Overfitting detection
* Model selection

---

## 🎓 Assignment Requirements Covered

| Assignment Requirement       | Status      |
| ---------------------------- | ----------- |
| Dataset exploration          | ✅ Completed |
| Missing value handling/check | ✅ Completed |
| Duplicate handling/check     | ✅ Completed |
| Categorical encoding         | ✅ Completed |
| Feature selection            | ✅ Completed |
| Feature scaling              | ✅ Completed |
| Train-test split             | ✅ Completed |
| Random Forest                | ✅ Completed |
| KNN                          | ✅ Completed |
| Decision Tree                | ✅ Completed |
| Naive Bayes                  | ✅ Completed |
| SVM                          | ✅ Completed |
| Accuracy                     | ✅ Completed |
| Precision                    | ✅ Completed |
| Recall                       | ✅ Completed |
| F1-Score                     | ✅ Completed |
| Confusion Matrix             | ✅ Completed |
| Cross-validation             | ✅ Completed |
| Hyperparameter tuning        | ✅ Completed |
| Model comparison             | ✅ Completed |
| Best model selection         | ✅ Completed |

---

## 🔮 Possible Improvements

Future improvements could include:

* Additional feature engineering.
* Testing additional classification algorithms.
* Exploring ensemble methods.
* Performing more extensive hyperparameter optimization.
* Investigating the features responsible for campaign success.
* Testing the final model on an independent external dataset.
* Deploying the final model as a web application or API.

---

## 📌 Conclusion

This project successfully implemented a complete machine learning classification workflow for predicting crowdfunding campaign success.

Five classification algorithms — **Random Forest, KNN, Decision Tree, Naive Bayes, and SVM** — were trained and evaluated using Accuracy, Precision, Recall, F1-score, and Confusion Matrix.

Cross-validation was used to evaluate model stability, while RandomizedSearchCV was used for hyperparameter tuning.

Among all the models, **SVM achieved the best performance**, with a **99.93% testing accuracy and 99.93% F1-score**. Its training and testing results were also very close, suggesting strong generalization to unseen data.

The Decision Tree was the second-best-performing model, while KNN showed a substantial difference between training and testing performance, indicating overfitting.

Overall, the project demonstrates the complete process of building, validating, tuning, comparing, and selecting a machine learning classification model for a real-world prediction problem.

---

## 👩‍💻 Author

**Varsha A**

B.Sc. Artificial Intelligence & Machine Learning

**Data Science & Machine Learning Project**
