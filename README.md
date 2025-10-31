# 🩺 Diabetes Prediction using Support Vector Machine (SVM)

This project uses a **Support Vector Machine (SVM)** model to predict whether a person is likely to have diabetes based on various medical parameters such as glucose level, BMI, age, insulin, and more.  
The dataset used is based on the **Pima Indians Diabetes Dataset**.

---

## 📊 Dataset Information

**Features:**
- Pregnancies  
- Glucose  
- BloodPressure  
- SkinThickness  
- Insulin  
- BMI  
- DiabetesPedigreeFunction  
- Age  

**Target:**
- Outcome → `1` means **Diabetic**, `0` means **Non-Diabetic**

---

## ⚙️ Steps Followed

1. **Data Loading**  
   - Loaded the dataset using `pandas`.

2. **Data Cleaning**  
   - Replaced invalid zero values (like `0` in Glucose or BloodPressure) with median values.  

3. **Data Splitting**  
   - Split the dataset into **80% training** and **20% testing** sets.  

4. **Feature Scaling**  
   - Standardized the data using `StandardScaler` for better SVM performance.

5. **Model Training**  
   - Trained an **SVM classifier** (`sklearn.svm.SVC`) on the training data.

6. **Evaluation**  
   - Evaluated the model on the test set using accuracy, confusion matrix, and classification report.

---

## 📈 Model Performance

| Metric | Value |
|--------|--------|
| **Accuracy** | **75%** |
| **Precision (avg)** | 0.74 |
| **Recall (avg)** | 0.75 |
| **F1-Score (avg)** | 0.74 |

---

## 🧠 Example Prediction

Input sample:
```python
test_point = [[4, 125, 78, 28, 85, 33.6, 0.52, 36]]
prediction = model.predict(test_point)
