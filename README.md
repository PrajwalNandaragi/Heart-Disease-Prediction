# Heart Disease Prediction Using Logistic Regression

This project uses a machine learning model to predict whether a person is likely to have heart disease based on several medical parameters. The model is trained using the **Logistic Regression** algorithm from the **scikit-learn** library.

---

## 📂 Dataset

The dataset used is `heart_disease_data.csv`, which contains 303 samples with 14 attributes:

| Feature     | Description |
|-------------|-------------|
| `age`       | Age of the patient |
| `sex`       | Sex (1 = male, 0 = female) |
| `cp`        | Chest pain type (0–3) |
| `trestbps`  | Resting blood pressure (in mm Hg) |
| `chol`      | Serum cholesterol in mg/dl |
| `fbs`       | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) |
| `restecg`   | Resting electrocardiographic results |
| `thalach`   | Maximum heart rate achieved |
| `exang`     | Exercise induced angina (1 = yes; 0 = no) |
| `oldpeak`   | ST depression induced by exercise relative to rest |
| `slope`     | The slope of the peak exercise ST segment |
| `ca`        | Number of major vessels (0–3) colored by fluoroscopy |
| `thal`      | Thalassemia (1 = normal; 2 = fixed defect; 3 = reversible defect) |
| `target`    | Diagnosis of heart disease (1 = presence, 0 = absence) |

---

## 🧪 Project Workflow

### 1. **Loading and Exploring the Data**
- The dataset was read using `pandas`.
- Checked for missing values — none were found.
- Verified data types and structure.

### 2. **Preprocessing**
- Split the dataset into **features (X)** and **labels (Y)**.
- Split data into **training** (80%) and **testing** (20%) sets using `train_test_split`.

### 3. **Model Training**
- Used **Logistic Regression** from `sklearn.linear_model`.
- The model was trained using `model.fit(X_train, Y_train)`.

> ⚠️ A convergence warning was shown during training. This indicates that the default number of iterations (`max_iter=100`) was not enough. You can fix this by increasing `max_iter` or normalizing the data.

### 4. **Evaluation**
- Training Accuracy: **~85.1%**
- Testing Accuracy: **~81.9%**
- Used `accuracy_score` from `sklearn.metrics` for evaluation.

### 5. **Prediction on New Data**
A sample prediction was made using the following input:
```python
input_data = (41, 0, 1, 130, 204, 0, 0, 172, 0, 1.4, 2, 0, 2)
```

Model output:
```
[1] => Person has Heart Disease
```

---

## 🛠 Requirements

- Python 3.x
- numpy
- pandas
- scikit-learn

You can install the dependencies using:
```bash
pip install numpy pandas scikit-learn
```

---

## 📈 Future Improvements

- Handle convergence warning by scaling features or increasing `max_iter`.
- Try other classifiers like Random Forest, SVM, or XGBoost.
- Add feature scaling (e.g., StandardScaler).
- Build a frontend UI using Streamlit or Flask for user interaction.

---



