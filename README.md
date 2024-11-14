# 🏛️ XplainHR-Attrition - The Shawshank Prediction Project

Welcome to **The Shawshank Prediction Project**, where machine learning meets a corporate prison drama! In this project, we dive deep into **employee attrition** analysis with the help of **Random Forest models** and **SHAP** (SHapley Additive exPlanations). Just like Andy Dufresne’s journey to freedom, this project explores the factors that drive employees to "escape" from their jobs and helps shed light on the reasons behind it.

---

## Medium Article

Here's the link to the Medium article: [The Shawshank Prediction: A Machine Learning Journey Through the Corporate Prison of Employee Attrition](https://medium.com/@akhilxox/the-shawshank-prediction-a-machine-learning-journey-through-the-corporate-prison-of-employee-23b8f0f685a0)


## 📖 Project Overview

Imagine a prison-like company, **Corporateville Inc.**, where employees are quietly breaking out (a.k.a. quitting) without anyone really understanding why. Enter our protagonist: **Andy Dufresne**, a data science intern who’s about to uncover the hidden factors leading to attrition. Using a **Random Forest model** to predict employee exits and **SHAP** to interpret the model’s decisions, this project helps Corporateville understand why their folks are running for the hills.

Our goal is to build a predictive model and interpret it in a way that even the warden (HR) can understand, all while keeping it light, a bit satirical, and maybe even inspiring enough to follow Andy’s escape.

---

## 🚀 Project Features

- **Random Forest Model**: A powerful, ensemble-based machine learning model trained to predict if an employee is likely to quit.
- **SHAP Analysis**: SHAP (SHapley Additive exPlanations) provides insights into which factors contribute most to employee attrition. It’s like a flashlight in the dark maze of a Random Forest.
- **SHAP Summary Plot**: A visual representation that helps identify key drivers of attrition, such as **overtime**, **job level**, and **years at company**.
- **Data Cleaning and Preparation**: Remove unnecessary columns, handle categorical data, and prepare the dataset for effective modeling.

---

## 📊 The Dataset

We use an **HR Analytics dataset** that contains various attributes of employees, including:

- **Employee Personal Information**: Age, Marital Status, etc.
- **Job Information**: Job Level, Department, Years at Company, Stock Option Level.
- **Work Conditions**: Overtime, Distance from Home, Environment Satisfaction.
- **Attrition Status**: Whether the employee has quit or stayed.

Our objective is to predict the **Attrition** status (Yes/No) and understand what factors contribute most to an employee’s decision to leave.

---

## ⚙️ Project Workflow

1. **Data Cleaning**: We clean the dataset by removing irrelevant columns and encoding categorical variables. Features like Employee ID and Over18 (everyone’s over 18) are removed to reduce noise.
   
2. **Model Building**: We build a **Random Forest Classifier** to predict whether an employee will quit or stay. Random Forest is chosen for its robustness and ability to handle complex relationships between features.

3. **Model Evaluation**: The model’s accuracy is evaluated using a test set. In our story, we achieved **86.15% accuracy**—not bad for a prison break attempt!

4. **SHAP Analysis**: We use SHAP to interpret the Random Forest model. SHAP provides insights into which factors (like **overtime** and **job level**) have the most significant impact on the prediction. It’s like Andy’s “blueprint” for understanding what drives employees to leave.

5. **SHAP Summary Plot**: The SHAP summary plot visualizes the average impact of each feature on model output. Each bar represents a factor, with longer bars indicating a stronger influence on attrition. This is our visual key to understanding Corporateville’s employee exodus.

---

## 🔍 Key Insights from SHAP

Our **SHAP summary plot** reveals the top factors that drive attrition:

- **OverTime_Yes**: Working overtime has the highest impact on attrition, suggesting that long hours push employees to leave.
- **JobLevel**: Higher job levels indicate more responsibility and may contribute to burnout.
- **YearsAtCompany**: The longer an employee has stayed, the more likely they are to leave—suggesting stagnation or a desire for change.
- **StockOptionLevel**: Stock options don’t seem to offer enough incentive to retain employees.
- **Age**: Older employees show a stronger tendency to leave, possibly due to retirement or career shifts.
  
These insights serve as a roadmap for Corporateville’s HR to improve retention strategies and foster a healthier work environment.

---

## 🧠 What is SHAP?

**SHAP** (SHapley Additive exPlanations) is an interpretability tool based on **game theory**. It calculates the **Shapley value** for each feature in the model, showing how much each feature “contributes” to the prediction:

$$
\phi_i = \sum_{S \subseteq N \setminus \{i\}} \frac{|S|! \, (|N| - |S| - 1)!}{|N|!} \left( f(S \cup \{i\}) - f(S) \right)
$$

This formula essentially averages the contribution of each feature across all possible combinations, providing a **marginal contribution**. However, calculating exact Shapley values is computationally intensive, so the SHAP library uses approximations. It’s an approximation of an approximation—close enough to give us insights, but fast enough to be practical.

In layman’s terms, SHAP helps us understand which features are making people want to leave Corporateville, even if it doesn’t know the exact formula.

> **Fun Fact**: SHAP is like a tech bro who’s 90% sure of the answer. It’s not perfect, but it’s confident enough to be useful!

---

## 📜 Installation

To run this project, simply click on the below button to open a Google Colab notebook and follow the instructions. 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AkhilByteWrangler/XplainHR-Attrition/blob/main/Attrition_Prediction_and_Explainability.ipynb)

## Citations

Anshika. HR Analytics Dataset. Kaggle, 2021, https://www.kaggle.com/datasets/anshika2301/hr-analytics-dataset/data. Accessed on Nov 13th 2024.

Disclaimer: This dataset was accessed and used solely for educational purposes
