# 🎓 Student Pass/Fail Prediction Using SVM Classification

🚀 A beginner-friendly Machine Learning project that predicts whether a student will **Pass** or **Fail** based on their **Attendance Percentage** using the **Support Vector Machine (SVM)** Classification algorithm.

📚 This project demonstrates the complete Machine Learning workflow including:

✅ Data Collection  
✅ Data Understanding  
✅ Data Visualization  
✅ Data Preprocessing  
✅ SVM Classification  
✅ Prediction  
✅ Performance Evaluation  

---

## 🚀 Open in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1E4g2RJCSii6XTtQzAJkwMKE5nOxjRENP?usp=sharing)

---

## 🛠️ Technologies Used

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-SVM-orange?logo=scikitlearn)
![Google Colab](https://img.shields.io/badge/Google-Colab-yellow?logo=googlecolab)

---

## 📌 Project Overview

🎯 **Goal:** Predict whether a student will Pass or Fail based on attendance percentage.

This project uses the Support Vector Machine (SVM) Classification algorithm to learn patterns from attendance records and classify students as Pass or Fail.

---

## 🔄 Project Workflow

```text
📂 Dataset Collection
        ↓
📖 Dataset Understanding
        ↓
🧹 Data Preprocessing
        ↓
📊 Data Visualization
        ↓
✂️ Train-Test Split
        ↓
🤖 SVM Classification
        ↓
📈 Prediction
        ↓
📋 Model Evaluation
```

---

## 📂 Dataset

Dataset: Student Attendance Dataset

| Column | Description |
|----------|------------|
| Attendance | Student Attendance Percentage |
| Result | Pass / Fail |

### 📊 Sample Dataset

| Attendance | Result |
|------------|--------|
| 95 | Pass |
| 90 | Pass |
| 85 | Pass |
| 80 | Pass |
| 75 | Pass |
| 68 | Fail |
| 60 | Fail |
| 50 | Fail |

---

## 📦 Installation

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 📚 Import Libraries

```python
import pandas as pd

from sklearn.model_selection import train_test_split
from sklearn.svm import SVC

from sklearn.metrics import (
    accuracy_score,
    confusion_matrix,
    classification_report
)
```

---

## 📥 Load Dataset

```python
df = pd.read_csv("student_attendance.csv")
```

---

## 🔍 Dataset Exploration

```python
print(df.head())

print(df.shape)

print(df.info())

print(df.describe())
```

---

## 🧹 Data Preprocessing

Convert labels into numerical values:

```python
df['Result'] = df['Result'].map({
    'Pass': 1,
    'Fail': 0
})
```

---

## 🤖 Machine Learning Model

### Define Input and Output

```python
X = df[['Attendance']]
y = df['Result']
```

### Train-Test Split

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

### Create SVM Model

```python
model = SVC(kernel='linear')
```

### Train Model

```python
model.fit(X_train, y_train)
```

### Prediction

```python
y_pred = model.predict(X_test)
```

---

## 📈 Model Evaluation

### Accuracy Score

```python
accuracy = accuracy_score(y_test, y_pred)

print("Accuracy:", accuracy)
```

### Confusion Matrix

```python
print(confusion_matrix(y_test, y_pred))
```

### Classification Report

```python
print(classification_report(y_test, y_pred))
```

---

## 🎯 Predict New Student Result

```python
attendance = [[72]]

prediction = model.predict(attendance)

if prediction[0] == 1:
    print("Pass")
else:
    print("Fail")
```

---

## 📊 Sample Output

```text
Accuracy: 1.0

[[2 0]
 [0 2]]

Pass
```

---

## ✨ Features

🌟 Beginner-Friendly Project

📊 Attendance Analysis

🤖 SVM Classification

📈 Pass/Fail Prediction

📋 Model Evaluation

🎓 Educational Dataset

🚀 Google Colab Ready

---

## 📚 Evaluation Metrics Used

✅ Accuracy Score

✅ Confusion Matrix

✅ Classification Report

---

## 🎓 Learning Outcomes

Through this project, I learned:

📌 Data Loading using Pandas

📌 Data Preprocessing

📌 Classification Problems

📌 Support Vector Machine (SVM)

📌 Train-Test Split

📌 Model Evaluation

📌 Prediction Techniques

---

## 🔮 Future Improvements

🚀 Add Multiple Features

🚀 Student Performance Dashboard

🚀 Streamlit Web Application

🚀 Attendance Management System

🚀 Real-Time Prediction System

---

## 📁 Project Structure

```text
Student-Pass-Fail-Prediction/
│
├── student_attendance.csv
├── svm_classification.ipynb
├── README.md
│
└── screenshots/
```

---

## 👨‍💻 Author

### Chatakondu Venkata Yaswanth

🎓 B.Tech Computer Science and Engineering

🏫 IIIT Kottayam

🔗 LinkedIn:
https://www.linkedin.com/in/chatakondu-venkata-yaswanth-8bab82321

---

## ⭐ Support

If you found this project useful, please give it a ⭐ on GitHub.

---

## 📜 License

📚 This project is created for educational, learning, and internship purposes.
