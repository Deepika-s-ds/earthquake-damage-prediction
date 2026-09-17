# Earthquake Damage Grade Prediction

## 📌 Project Overview

This project focuses on predicting earthquake-related building damage grades
using machine learning techniques.

The objective is to analyse structural, geographical, and ownership-related
building features and predict the severity of earthquake damage.

The project belongs to the domain of **Disaster Management and Civil Engineering**.

---

## 🎯 Problem Statement

Earthquake damage varies depending on building construction materials, age,
height, foundation type, geographical location, and other structural
characteristics.

This project develops a machine learning classification model to predict the
damage grade of buildings affected by an earthquake.

The target variable is `damage_grade`:

- `1` — Low damage
- `2` — Moderate damage
- `3` — Severe damage or almost complete destruction

---

## 🎯 Project Objectives

- Perform exploratory data analysis on the earthquake building dataset
- Understand the factors affecting earthquake damage severity
- Clean and preprocess the dataset
- Encode categorical variables
- Build multiple machine learning classification models
- Compare model performance using classification metrics
- Select the best-performing model
- Analyse feature importance
- Identify factors associated with building damage
- Provide insights that may support earthquake damage assessment

---

## 📂 Dataset Information

The dataset contains building-related information such as:

- Geographical features
- Building age
- Number of floors
- Building area and height
- Foundation type
- Roof type
- Ground-floor type
- Other-floor type
- Land-surface condition
- Construction materials
- Ownership status
- Secondary-use information

The feature dataset contains 260,601 records and 39 feature columns.
After merging the features with the target labels, the modelling dataset
contains 260,601 records and 40 columns.

The dataset contains numerical and categorical features.

---

## 🔍 Project Workflow

### 1. Data Loading

- Loaded the building feature dataset
- Loaded the damage-grade target dataset
- Merged the datasets using `building_id`

### 2. Data Quality Assessment

- Checked dataset dimensions
- Reviewed data types
- Analysed missing values
- Checked duplicate records
- Examined statistical summaries

### 3. Exploratory Data Analysis

- Analysed damage-grade distribution
- Studied building age and structural characteristics
- Examined geographical features
- Analysed construction-material features
- Investigated relationships between building characteristics and damage grade

### 4. Data Preprocessing

- Separated features and target
- Encoded categorical variables
- Prepared data for machine learning
- Addressed class imbalance during model preparation

### 5. Model Development

The following classification models were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

### 6. Model Evaluation

The models were evaluated using:

- Accuracy
- Weighted F1 Score
- Precision
- Recall
- Classification Report
- Confusion Matrix

### 7. Feature Importance

Feature-importance analysis was performed to understand which building,
geographical, and structural features contributed most strongly to model
predictions.

---

## 📊 Model Performance

| Model | Accuracy | Weighted F1 Score |
|---|---:|---:|
| Logistic Regression | 42.10% | 41.68% |
| Decision Tree | 64.68% | 64.95% |
| Random Forest | 70.54% | 70.58% |
| XGBoost | 69.23% | 69.44% |

### Final Model

The Random Forest model achieved the highest performance among the evaluated
models.

- **Final Accuracy:** 70.54%
- **Final Weighted F1 Score:** 70.58%

The final classification report includes precision, recall, and F1-score for
damage grades 1, 2, and 3.

---

## 📈 Model Results

### Model Comparison

![Model Comparison](images/model_comparison.png)

### Final Model Evaluation

![Final Model Evaluation](images/final_model_evaluation.png)

### Feature Importance

![Feature Importance](images/feature_importance.png)

---

## 💡 Key Insights

- Building location-related features were among the most important predictors.
- `geo_level_1_id`, `geo_level_3_id`, and `geo_level_2_id` had strong feature
  importance.
- Building age was also an important feature.
- Area percentage and structural construction features contributed to model
  predictions.
- Random Forest achieved the highest accuracy and weighted F1 score among the
  evaluated models.

---

## 💼 Real-World Applications

This type of model may support:

- Earthquake damage assessment
- Identification of vulnerable buildings
- Disaster-response planning
- Infrastructure risk analysis
- Prioritisation of inspection and recovery activities
- Earthquake preparedness and mitigation planning

---

## ⚠️ Limitations

- The model is based on the available dataset and its recorded features.
- Predictions may vary for buildings or regions that are not represented in
  the training data.
- Further validation is required before applying the model in real-world
  disaster-management systems.
- Additional external information may improve prediction performance.

---

## 🚀 Future Scope

- Perform advanced hyperparameter tuning
- Explore additional ensemble models
- Improve class-imbalance handling
- Apply cross-validation
- Analyse model explainability in greater detail
- Test the model on additional earthquake datasets
- Develop a dashboard for damage-risk assessment
- Build a deployment-ready prediction application

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📁 Repository Structure

```text
earthquake-damage-prediction/
│
├── Earthquake_Damage_Prediction.ipynb
├── README.md
├── requirements.txt
│
└── images/
    ├── model_comparison.png
    ├── final_model_evaluation.png
    └── feature_importance.png
