## 🧪 Liver Disease Stage Classification - EDA & XGBoost Modeling

This project focuses on analyzing a medical dataset to classify the **stage of liver disease** using various biochemical and demographic features. It covers the full cycle from **exploratory data analysis** to **model development and tuning**, aimed at building a robust classification model using **XGBoost**.

---

### 🎯 Main Objectives

* Explore the distribution and relationships between liver-related medical features
* Handle missing values and outliers in the dataset
* Visualize class imbalance and perform class-wise feature analysis
* Train a classification model to predict liver disease stage
* Optimize model performance using **GridSearchCV**
* Identify key features contributing to model predictions

---

### 🩺 Dataset Description

The dataset contains **clinical features** such as:

* Biochemical markers (e.g., SGOT, Albumin, Bilirubin)
* Coagulation indicators (e.g., INR, Prothrombin)
* Mineral levels (e.g., Copper)
* Target variable: `Stage` (multi-class) indicating disease severity

---

### 📊 Key Analysis & Visualizations

* **Correlation heatmap** for identifying multicollinearity
* **Boxplots** and **distribution plots** for visualizing outliers and feature spread
* **Bar plots** comparing distributions of key features across disease stages
* **Class imbalance** visualized clearly to highlight model challenges

---

### 🧠 Modeling Process

* Model used: **XGBoost Classifier**
* Evaluation metrics: Precision, Recall, F1-Score, Accuracy
* Issues addressed:

  * Class imbalance
  * Low recall for certain stages
* After tuning:

  * Performance improved for minority classes (especially Stage 1 and 2)
  * Model still struggles with Stage 0 (very rare class)

---

### ⚙️ Fine-Tuning Details

* Performed grid search on:

  * `learning_rate`, `max_depth`, `n_estimators`, `subsample`
* Best parameters identified and used to retrain the model

---

### 🏆 Best Model Comparison

* **Random Forest vs XGBoost (Before and After Tuning)**
* XGBoost after fine-tuning performs better on harder-to-predict classes
* Random Forest shows higher precision for some majority classes

---

### 📈 Feature Importance

Top predictive features:

* **SGOT**, **Platelets**, **Copper**
* Also important: Triglycerides, Albumin, Alkaline Phosphatase, Age, Hepatomegaly

Importance is based on **F-score**, indicating how often a feature is used in splits and its contribution to reducing model error.

---

### 📌 Conclusion

* XGBoost is effective for liver disease stage prediction, especially after tuning.
* The model handles majority classes well but needs further improvements for rare stages.
* Medical features like SGOT and Copper play a critical role in disease staging.
