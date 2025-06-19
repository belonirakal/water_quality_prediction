# 💧 Water Quality Prediction Using Machine Learning

This project uses a Random Forest Classifier to predict water quality (Good or Poor) based on various physicochemical parameters such as NH₄, O₂, BSK5, NO₃, etc., from historical water quality data.

---

## 📂 Dataset

- **File:** `PB_All_2000_2021.csv`
- **Source:** Uploaded manually via Google Colab
- **Delimiter:** Semicolon (`;`)
- **Features:**  
  - `NH4`: Ammonium  
  - `O2`: Dissolved Oxygen  
  - `BSK5`: Biochemical Oxygen Demand  
  - `NO3`, `NO2`, `SO4`, `PO4`, `CL`, `Suspended`, etc.

---

## 🔧 Steps Performed

1. **Data Loading & Cleaning**
   - Reads CSV with correct delimiter
   - Converts `date` column to datetime
   - Drops missing values

2. **Label Generation**
   - Water classified as **Good (1)** if:
     - NH₄ ≤ 0.5  
     - O₂ ≥ 5.0  
     - BSK5 ≤ 5.0  
   - Otherwise labeled as **Poor (0)**

3. **Feature Scaling**
   - Used `StandardScaler` from `sklearn`

4. **Model Training**
   - Trained a **Random Forest Classifier** with `n_estimators=100`

5. **Evaluation**
   - Printed confusion matrix and classification report
   - Plotted feature importance using `seaborn`

6. **Output**
   - Saved cleaned and labeled dataset as `cleaned_data.csv`
   - Downloaded directly from Colab

---

## 🧠 Requirements

Run in **Google Colab** with:
```bash
pandas
numpy
scikit-learn
matplotlib
seaborn
