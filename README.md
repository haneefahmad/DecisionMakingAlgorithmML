# Breast Cancer Prediction using Decision Tree Machine Learning

## Overview

This project uses a Decision Tree Classifier to predict whether a breast tumor is malignant or benign using the Breast Cancer Wisconsin Dataset available in Scikit-Learn.

The notebook demonstrates the complete machine learning workflow:

- Data Loading
- Data Exploration
- Data Preprocessing
- Train-Test Split
- Model Training
- Model Evaluation
- Decision Tree Visualization
- GitHub Version Control Integration

---

## Dataset

The project uses the Breast Cancer Wisconsin Diagnostic Dataset provided by Scikit-Learn.

Features include:

- Mean Radius
- Mean Texture
- Mean Perimeter
- Mean Area
- Mean Smoothness
- Mean Compactness
- Mean Concavity
- Mean Symmetry
- Worst Radius
- Worst Texture
- And many more

Dataset Statistics:

- Total Samples: 569
- Features: 30
- Target Classes:
  - 0 → Malignant
  - 1 → Benign

---

## Technologies Used

- Python 3
- Pandas
- Scikit-Learn
- Matplotlib
- Google Colab
- Git & GitHub

---

## Installation

Clone the repository:

```bash
git clone https://github.com/haneefahmad/DecisionMakingAlgorithmML.git
cd DecisionMakingAlgorithmML
```

Install dependencies:

```bash
pip install pandas scikit-learn matplotlib
```

---

## Project Workflow

### 1. Import Required Libraries

```python
from sklearn.datasets import load_breast_cancer
import pandas as pd
```

### 2. Load Dataset

```python
data = load_breast_cancer()
```

### 3. Create DataFrame

```python
df = pd.DataFrame(data.data, columns=data.feature_names)
df['target'] = data.target
```

### 4. Data Preprocessing

- Handle missing values using median imputation
- Separate features and target labels

```python
df.fillna(df.median(), inplace=True)
```

### 5. Split Dataset

```python
from sklearn.model_selection import train_test_split
```

Training Data: 80%

Testing Data: 20%

---

### 6. Train Decision Tree Model

```python
from sklearn.tree import DecisionTreeClassifier

tree = DecisionTreeClassifier()
tree.fit(X_train, y_train)
```

---

### 7. Make Predictions

```python
y_pred = tree.predict(X_test)
```

---

### 8. Evaluate Model

```python
from sklearn.metrics import accuracy_score

accuracy = accuracy_score(y_test, y_pred)
```

### Model Accuracy

```
Decision Tree Accuracy: 92.11%
```

---

### 9. Visualize Decision Tree

```python
from sklearn.tree import plot_tree
import matplotlib.pyplot as plt

plt.figure(figsize=(12,8))
plot_tree(
    tree,
    filled=True,
    feature_names=X.columns,
    class_names=['Class 1', 'Class 2']
)
plt.show()
```

---

## Results

| Metric | Value |
|----------|---------|
| Algorithm | Decision Tree Classifier |
| Dataset Size | 569 Samples |
| Features | 30 |
| Test Split | 20% |
| Accuracy | 92.11% |

---

## Project Structure

```text
DecisionMakingAlgorithmML/
│
├── DecisionMakingAlgorithm.ipynb
├── README.md
└── requirements.txt
```

---

## Future Improvements

- Hyperparameter Tuning
- Cross Validation
- Random Forest Implementation
- Gradient Boosting Models
- Feature Selection
- Confusion Matrix Visualization
- Precision, Recall, and F1 Score Analysis

---

## Author

**Haneef Ahmad**

GitHub: https://github.com/haneefahmad

LinkedIn: https://www.linkedin.com/in/haneefahmad

---

## License

This project is open-source 
