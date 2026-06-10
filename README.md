# Predictive Analysis of Dengue Fever Cases Using XGBoost and LSTM Machine Learning Models

## 📌 1. Overview
This project develops and compares machine learning models to predict **dengue cases in Indonesia**.

The objective is not only to achieve high predictive performance, but also to evaluate each model’s ability to capture **temporal dynamics, stability, and practical applicability** for real-world use.

---


## 📂 2. Dataset

The dataset is sourced from official Indonesia Health Profile reports (2018–2022) and is stored in the file `DBD_Indonesia.xlsx`.

### 📌 Data Characteristics
- Coverage: 34 provinces in Indonesia  
- Observations: 170 records  
- Data type: Panel / structured data  
- Variables: 20+ socio-demographic and healthcare features  

### 📌 Key Variables
- Population density  
- Human Development Index (HDI)  
- Poverty rate  
- Healthcare facilities (hospitals, clinics, etc.)  
- Public health indicators  
- Dengue case counts (target variable)  

---


## ⚙️ 3. Project Workflow

### 3.1. Data Preparation
- Data cleaning and validation (no missing values found)  
- One-hot encoding for categorical features  
- Feature scaling (Min-Max normalization for LSTM)  
- Train-test split (80% train, 20% test)  

---

### 3.2. Exploratory Data Analysis (EDA)
- Analysis of dengue case distributions  
- Identification of key socio-demographic drivers  
- Comparison across provinces  
- Data validation and consistency checks  

---

### 3.3. Model Development

Two models were implemented to compare different modeling approaches:

---

#### 🟢 XGBoost (Machine Learning Approach)
- Tree-based gradient boosting model  
- Strong for structured tabular data  
- Provides feature importance for interpretability  
- Limited in capturing time-dependent patterns  

---

#### 🔵 LSTM (Deep Learning Approach)
- Recurrent neural network designed for sequential data  
- Captures temporal patterns in dengue cases  
- More suitable for time-series prediction  
- Less interpretable and computationally intensive  

---


### 3.4. Model Validation

#### A. Evaluation Metric
- **Mean Squared Error (MSE)**  

#### B. Validation Approach
- Train-test evaluation  
- Cross-validation for XGBoost  
- Training vs validation loss monitoring (LSTM)  


### 3.5. Implementation Details
The analysis and modeling processes were implemented using Python in a Google Colab environment, with the code stored in the notebook `dbd_analysis.ipynb`.

---

## 🏆 4. Model Performance Comparison

| Model   | Train MSE | Test MSE |
|--------|----------|----------|
| **LSTM** | ~2.87M   | ~3.86M   |
| XGBoost | ~9.01M   | ~4.83M   |

---

### ✅ Selected Model: **LSTM**

After evaluating predictive performance and model consistency, **LSTM** was identified as the most suitable model.

The model demonstrated:
- Lower prediction error (MSE)  
- Better ability to capture **temporal patterns**  
- More stable performance on unseen data  

---


### ⚠️ Why Not XGBoost?

While XGBoost provides strong interpretability through feature importance, it was not selected due to:

- Higher prediction error  
- Limited ability to capture sequential patterns  
- Better suitability for cross-sectional data rather than time-series forecasting  

As a result, XGBoost is effective for understanding variable relationships, but less suitable for modeling dengue case trends over time.

---

## 📊 5. Key Insights

- Healthcare infrastructure (hospitals, clinics) is the strongest predictor of dengue cases  
- Socio-demographic factors such as population density and HDI play a significant role  
- Temporal patterns are critical in disease prediction  
- LSTM outperforms traditional ML models in capturing these dynamics  

---

## 💼 6. Business / Policy Implications

- Supports **early detection of potential outbreaks**  
- Enables **data-driven public health planning**  
- Improves **resource allocation in healthcare**  
- Provides insights for epidemic risk management  


---

## 📈 7. Tools & Technologies

- Python  
- XGBoost  
- TensorFlow / Keras (LSTM)  
- Data preprocessing and analysis libraries  

---

## ⚠️ 8. Notes
- Dataset is based on official government reports  
- Project is developed for academic purposes  
- Future improvements may include climate and environmental variables  

---

## 👤 9. Author

Dylan Richard


