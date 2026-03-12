#  Space Passenger Survival Prediction

##  Problem Statement
The goal of this project is to predict whether a passenger aboard the **Spaceship Titanic** was transported to another dimension due to a spacetime anomaly. The dataset contains passenger information such as their home planet, destination, age, VIP status, cryosleep status, and spending behavior. Using these features, machine learning models are trained to classify passengers into two categories: **Transported (True)** or **Not Transported (False)**. The objective is to build a model that can accurately predict passenger transportation.

---

#  Dataset Description

The dataset used in this project comes from the **Spaceship Titanic Kaggle competition**. It contains information about passengers traveling on the spaceship.

### Dataset Size
- **Training Data:** 8693 rows, 14 columns  
- **Test Data:** 4277 rows, 13 columns  

### Features Description

| Feature | Description |
|------|------|
| PassengerId | Unique identifier for each passenger |
| HomePlanet | The planet from which the passenger boarded |
| CryoSleep | Indicates whether the passenger was in cryosleep during the journey |
| Cabin | Cabin number where the passenger stayed |
| Destination | Planet where the passenger was traveling |
| Age | Age of the passenger |
| VIP | Indicates whether the passenger is a VIP |
| RoomService | Amount spent on room service |
| FoodCourt | Amount spent on food court services |
| ShoppingMall | Amount spent on shopping |
| Spa | Amount spent on spa services |
| VRDeck | Amount spent on virtual reality entertainment |
| Name | Name of the passenger |
| Transported | Target variable indicating whether the passenger was transported |

---

#  Data Preprocessing

The following preprocessing steps were performed on the dataset:

- Handling missing values using **mode for categorical features** and **median for numerical features**
- Splitting the **Cabin column into Deck, Number, and Side**
- Encoding categorical variables using **Label Encoding**
- Feature scaling using **StandardScaler**
- Splitting dataset into **training and validation sets**

---

#  Evaluation Metrics

The following evaluation metrics were used to measure model performance.

### Accuracy
Accuracy measures the percentage of correct predictions made by the model.

```
Accuracy = (TP + TN) / (TP + TN + FP + FN)
```

### Precision
Precision measures how many predicted positive cases are actually positive.

```
Precision = TP / (TP + FP)
```

### Recall
Recall measures how many actual positive cases were correctly identified.

```
Recall = TP / (TP + FN)
```

### F1 Score
F1 Score is the harmonic mean of precision and recall.

```
F1 Score = 2 * (Precision * Recall) / (Precision + Recall)
```

---

# Implemented Machine Learning Algorithms

## Random Forest
Random Forest is an ensemble learning algorithm that builds multiple decision trees and combines their predictions. It reduces overfitting and improves prediction accuracy by averaging the outputs of multiple trees.

## XGBoost
XGBoost (Extreme Gradient Boosting) is a powerful gradient boosting algorithm designed for speed and performance. It builds trees sequentially where each new tree corrects the errors of the previous trees.

## LightGBM
LightGBM is a gradient boosting framework that uses a leaf-wise tree growth strategy. It is optimized for faster training speed and higher efficiency, especially on large datasets.

---

#  Model Performance Results

| Model | Accuracy |
|------|------|
| Random Forest | 0.79 |
| XGBoost | 0.80 |
| LightGBM | **0.81** |

LightGBM achieved the best performance among the tested models.

---

#  Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- LightGBM
- Matplotlib
- Seaborn

---

#  Project Workflow

1. Data Loading  
2. Data Cleaning  
3. Exploratory Data Analysis (EDA)  
4. Feature Engineering  
5. Data Encoding  
6. Feature Scaling  
7. Model Training  
8. Model Evaluation  
9. Kaggle Submission  

---

#  Output

The final model generates predictions for the test dataset and creates a **submission.csv** file containing:

- PassengerId
- Transported (Prediction)

This file is used for Kaggle submission.
