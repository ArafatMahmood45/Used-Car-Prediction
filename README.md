# 🚗 Used Car Price Prediction with CatBoost  

## 📌 Project Overview  
This project predicts **used car prices** based on various features such as mileage, model year, brand, horsepower, transmission, fuel type, and more. The goal is to build a reliable machine learning model that captures real-world pricing patterns in the automobile market.  

## 🎯 Objectives  
- Perform data cleaning, handling missing values, and parsing unstructured engine data.  
- Conduct exploratory data analysis (EDA) to understand key factors influencing car prices.  
- Apply feature engineering and transformations (e.g., log-transform for skewed target).  
- Train and tune advanced machine learning models (**CatBoost & XGBoost**).  
- Evaluate models using **RMSE and MAE** 

## 📂 Dataset  
- Source: [Kaggle: https://www.kaggle.com/competitions/hackathon-qualification]  
- Size: 188533 rows, 13 features  
- Target Variable: `price`  

## 🛠️ Tools & Libraries  
- Python 
- Pandas, NumPy, Matplotlib, Seaborn (EDA & preprocessing)  
- Scikit-learn (metrics, preprocessing)  
- CatBoost & XGBoost (modeling)  

## 🔑 Key Steps  
1. **Data Preprocessing**  
   - Handled missing values  
   - Extracted engine specs (horsepower, liters, cylinders) using regex  
   - Encoded categorical features (CatBoost handles them natively)  

2. **Exploratory Data Analysis (EDA)**  
   - Mileage, model year, and brand emerged as strong predictors  
   - Price distribution highly skewed → applied log transform  

3. **Modeling**  
   - Compared CatBoost and XGBoost  
   - CatBoost performed best after hyperparameter tuning  

4. **Results**  
   - **CatBoost RMSE:** ~67,881  
   - **CatBoost MAE:** ~19,360    

5. **Feature Importance (CatBoost)**  
   - Mileage, model year, and brand were top predictors  
   - Aesthetic features (colors) also influenced pricing  

## 📊 Insights  
- Cars with **lower mileage, newer model years, and reputable brands** are priced higher.  
- **Colors and aesthetics** significantly impact pricing beyond technical specs.  
- **Accident history and engine details** have smaller effects compared to model year and usage.  

## 🚀 Next Steps  
- Improve feature engineering (e.g., interaction terms, external economic data).  
- Try ensemble/blending of CatBoost + XGBoost.  
- Deploy model using **FastAPI + Docker** for real-time predictions.  

## 📌 How to Run  
1. Clone the repository  
   ```bash
   git clone https://github.com/ArafatMahmood45/Used-Car-Prediction.git
   cd used-cars-prediction

   pip install -r requirements.txt

   jupyter notebook used-cars-prediction.ipynb
