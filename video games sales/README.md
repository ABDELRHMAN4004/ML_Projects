# 🎮 Video Games Sales Prediction  

## 📌 Project Overview  
This project aims to **predict global video game sales (`Global_Sales`)** using machine learning techniques. The dataset includes features such as year of release, genre, publisher, and platform.  
After preprocessing, we trained an **AdaBoost Regressor** model to estimate global sales with high accuracy.  

---

## 📂 Repository Structure  
- `data/` — dataset files.  
- `notebooks/` — Jupyter Notebooks for exploration and modeling.  
- `src/` — source code for preprocessing and training.  
- `README.md` — project documentation.  

---

## 🗃️ Dataset  
- **Rows:** 16,598  
- **Columns:** 11  

### Main Features:
- `Rank` — sales ranking.  
- `Name` — game title *(dropped later)*.  
- `Platform` — gaming platform.  
- `Year` — release year *(271 missing values)*.  
- `Genre` — game genre.  
- `Publisher` — publishing company *(58 missing values)*.  
- `NA_Sales`, `EU_Sales`, `JP_Sales`, `Other_Sales`, `Global_Sales` — sales in millions across regions and worldwide.  

---

## 🧹 Data Preprocessing  
1. **Missing Values:**
   - `Year` → filled with **mean value**.  
   - `Publisher` → filled with **mode value**.  
2. **Outliers:**  
   - Detected using **Boxplots** and fixed with the **IQR method** (replaced outliers with Q1/Q3 boundaries).  
3. **Dropped Columns:**  
   - `Name` was removed as it doesn’t affect predictions.  
4. **Feature Encoding:**  
   - `Genre` and `Publisher` mapped to their **value counts**.  

---

## 📊 Exploratory Data Analysis (EDA)  
- **Boxplots** plotted for sales (`NA_Sales`, `EU_Sales`, `JP_Sales`, `Other_Sales`, `Global_Sales`) to detect outliers.  
- Explored correlations and relationships between features and `Global_Sales`.  

---

## 🤖 Modeling  
- **Data Split:** 80% training, 20% testing.  
- **Model Used:**  
  - `AdaBoostRegressor()`  

### 📈 Model Performance
- **RMSE:** `0.0185`  
- **R² Score (Accuracy):** `0.994`  

---

## ⚙️ How to Run  
### Requirements  
- Python ≥ 3.8  
- Install dependencies:  
  ```bash
  pip install pandas numpy seaborn matplotlib scikit-learn
  ```  

### Steps  
1. Download the dataset (`video games sales.csv`) and place it in the `data/` folder.  
2. Open the Jupyter notebook or run the Python script.  
3. Execute cells/commands in order for preprocessing and model training.  

---

## 🚀 Future Improvements  
- Try other models (RandomForest, XGBoost, LightGBM).  
- Tune hyperparameters using GridSearch or Optuna.  
- Experiment with different encoding strategies (e.g., One-Hot Encoding).  
- Deploy the model as an API or web application.  

---

## ✍️ Author  
- **Abdelrahman Khalil Abdallah**  
