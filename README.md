# Decision-Trees-and-Random-Forests
# 🩺 Heart Disease Prediction – Decision Tree & Random Forest 

## 📌 Objective
This project applies **Decision Tree** and **Random Forest** classifiers to the **Heart Disease Dataset** for binary classification (Heart Disease vs No Heart Disease).  
Steps followed:
1. Train and visualize a Decision Tree.
2. Control overfitting by restricting depth.
3. Train and compare a Random Forest Classifier.
4. Interpret feature importances.
5. Evaluate using cross‑validation.

---

## 📂 Dataset
**File:** `heart.csv`  
**Source:** UCI Heart Disease Dataset  

Target Column: `target`  
- `1` = Disease present  
- `0` = No disease  

Includes features like:
`age`, `sex`, `cp` (chest pain type), `trestbps`, `chol`, `thalach`, `oldpeak`, `ca`, `thal`, and more.

---

## 🛠 Tools & Libraries
- Python 3.x
- pandas
- scikit-learn
- matplotlib
- graphviz (optional for better tree visuals)

**Install dependencies:**


---

## 📋 Methodology
1. **Data Loading & Exploration** – Verified structure, handled data as per requirement.  
2. **Train/Test Split** – 80% train, 20% test (stratified).  
3. **Model Training**  
   - Decision Tree (no depth limit)  
   - Decision Tree (max_depth=4)  
   - Random Forest (n_estimators=100)  
4. **Evaluation** – Used Accuracy, Precision, Recall, F1-score, and 5-fold Cross-Validation.  
5. **Visualization** – Decision Tree plot + Random Forest feature importance.

---

## 📊 Results & Observations

| Model                              | Test Accuracy | Precision (Class 0 / 1) | Recall (Class 0 / 1) | CV Accuracy (5‑fold) |
|------------------------------------|--------------:|------------------------:|---------------------:|---------------------:|
| Decision Tree (no limit)           | **0.985**     | 0.97 / 1.00              | 1.00 / 0.97           | —                    |
| Decision Tree (max_depth=4)        | 0.839         | —                        | —                     | **0.834**            |
| Random Forest (100 trees)          | **1.000**     | 1.00 / 1.00              | 1.00 / 1.00           | **0.997**            |

**Analysis:**
- **Unrestricted Decision Tree** – Achieved **98.5% test accuracy** but prone to overfitting due to unlimited depth.  
- **max_depth=4 Decision Tree** – Lower accuracy (**~84%**) but more generalizable and interpretable.  
- **Random Forest** – Perfect **100% test accuracy** and **~99.7% CV accuracy**, showing exceptional generalization while reducing variance.  
- **Top Features** (from Random Forest importance):  
  `cp` (chest pain type), `thal`, `ca` (number of major vessels), `oldpeak`, `thalach`.

---

## 📷 Visual Outputs
- `tree.png` – Visualization of Decision Tree (`max_depth=4`)  
- `feature_importance.png` – Random Forest feature importance bar chart  

---

## 🚀 How to Run
