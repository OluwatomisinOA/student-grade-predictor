# 🎓 Student Grade Predictor

A machine learning project that uses a simple linear regression model to predict a student's final grade (G3) based on their first two-period grades (G1, G2) and other social/school-related data.

This project is part of my self-learning journey in AI/ML, built by following the "Tech With Tim" machine learning tutorial.

## 📦 Dataset

* **Source:** [Student Performance Data Set](https://archive.ics.uci.edu/ml/datasets/Student+Performance) from the UCI Machine Learning Repository.
* **File Used:** `student_mat.csv` (data from the math course)
* **Key Features:** The model was trained on the following features:
    * `G1`: First period grade
    * `G2`: Second period grade
    * `studytime`: Weekly study time
    * `failures`: Number of past class failures
    * `absences`: Number of school absences

## 🤖 Model: Linear Regression

I used `scikit-learn`'s `LinearRegression` model to solve this regression problem. The goal is to predict the numerical value of the final grade, `G3`.

### 📊 Results & Findings

The model was trained on 90% of the data and tested on 10%.

* **Model Performance ($R^2$ Score):** The model achieved an **R-squared score of 74.77%** on the test data.
    

This $R^2$ score means that our model can explain roughly 74.77% of the variance in the final grades, which is a very strong result for a simple model.

### 📈 Interpreting the Model (Coefficients)

The model's coefficients tell us *how* it's making predictions:

* **G1 (First Grade):** `0.148`
* **G2 (Second Grade):** `0.976`
* **Study Time:** `-0.077`
* **Failures:** `-0.356`
* **Absences:** `0.038`

**Key Insights from this:**
* As expected, **G2 (the second-period grade)** is the *strongest* predictor of the final grade `G3`.
* **Failures** has a significant negative impact, meaning past failures are a strong indicator of a lower final grade.
* **Study time** and **absences** have a smaller, but still noticeable, effect.

## 🚀 How to Run

1.  Clone this repository.
2.  Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run the script:
    ```bash
    python student_model.py
    ```
