# 📊 Sales Revenue Prediction with Machine Learning  

## 🎯 Objective
This project applies **Machine Learning (ML)** to predict **sales revenue** for Rossmann stores. It helps businesses:  
- Improve forecasting accuracy  
- Reduce costs  
- Optimize marketing and promotions  

## 📂 Project Content
1. **Introduction**  
   - Dataset: Rossmann Store Sales (373,855 rows, 18 columns, year 2014).  
   - Task: Predict **Sales** using historical and store-specific features.  

2. **EDA (Exploratory Data Analysis)**  
   - Descriptive statistics and data visualization.  
   - Key insights: Sales patterns by day, month, promotions, holidays, and store type.  

3. **Data Preprocessing**  
   - Handle missing values and remove outliers.  
   - Encode categorical variables (Label Encoding, One-Hot Encoding).  
   - Feature scaling (MinMaxScaler, RobustScaler, Cyclic Transformation).  
   - Feature selection with **Boruta Algorithm**.  

4. **Model Building & Evaluation**  
   Multiple models were trained and compared:  
   - **Linear Regression**  
   - **Lasso Regression**  
   - **K-Nearest Neighbors (KNN)**  
   - **Random Forest Regressor** (best performing)  

   ### 📊 Model Comparison  

| Model                               | R² Score  | MAE        | MSE         | RMSE       | MAPE      |
| ----------------------------------- | --------- | ---------- | ----------- | ---------- | --------- |
| Linear Regression                   | 0.601     | 1393.37    | 3,709,738   | 1926.07    | 0.222     |
| Lasso Regression (Regularized)      | 0.600     | 1394.96    | 3,719,889   | 1928.70    | 0.223     |
| K-Nearest Neighbors (KNN) Regressor | 0.846     | 798.02     | 1,434,236   | 1197.60    | 0.118     |
| **Random Forest Regressor**         | **0.930** | **540.03** | **652,393** | **807.71** | **0.081** |

5. **Key Findings**
   - Most important features:  
     ```
     CompetitionDistance, Store, Promo, DayOfWeek,
     CompetitionOpenSinceMonth, CompetitionOpenSinceYear,
     Month, Promo2SinceYear, Promo2SinceWeek, StoreType_b
     ```  
   - Random Forest provided the most robust predictions.  

6. **Conclusion & Future Work**  
   - Random Forest achieved strong performance with ~90% R² on test.  
   - Future improvements:  
     - Compare with **XGBoost, LightGBM, CatBoost**  
     - Explore **time-series forecasting models** (ARIMA, Prophet, LSTM)  
     - Deploy the model via **Flask/FastAPI** for real-time prediction  

---

## 🚀 How to Run
1. Open **SourceCode.ipynb** with Jupyter Notebook or Google Colab.  
2. Run cells sequentially to:  
   - Load data  
   - Preprocess features  
   - Train models  
   - Compare results  

---

## 📘 Learning Extensions
- 📊 Advanced visualizations with seaborn/plotly  
- ⚡ Feature engineering (lag features, rolling mean)  
- 🏆 Benchmarking different ML models  
- ⏳ Time-series forecasting for long-term predictions  
- 📈 Model deployment as API services  

---

## 👨‍💻 Authors
- Nguyễn Ích Trường  
