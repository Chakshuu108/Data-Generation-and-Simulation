# 📊 Data Generation Using Modeling & Simulation for Machine Learning (FreeMat)

This project demonstrates how to use **modeling and simulation** to generate synthetic data and then apply **multiple machine learning models** to predict the simulation output. The goal is to compare different ML models and identify the **best-performing model** based on **Mean Squared Error (MSE)**.

---

## 🚀 Project Pipeline

1. **Select Simulation Tool**  
   - Tool used: **FreeMat** (MATLAB-like open-source environment)

2. **Define Simulation Model**  
   - Inputs (parameters):
     - `arrival_rate` ∈ [5, 50]
     - `service_time` ∈ [1, 10]
   - Output (simulated system performance):
     ```
     output = 0.05 * (arrival_rate)^2 + 2 * service_time + noise
     ```

3. **Generate Data**
   - 1000 random samples generated using the simulation model
   - Dataset columns:
     - arrival_rate
     - service_time
     - sim_output

4. **Split Dataset**
   - 80% Training
   - 20% Testing

5. **Train Multiple ML Models (10 Models)**
   - Mean Baseline
   - Linear Regression
   - Polynomial Regression (Degree 2)
   - Polynomial Regression (Degree 3)
   - Polynomial Regression (Degree 4)
   - Ridge Regression
   - KNN (k = 3)
   - KNN (k = 5)
   - KNN (k = 7)
   - Weighted Linear Regression

6. **Evaluate Models**
   - Metric used: **Mean Squared Error (MSE)**
   - Lower MSE = Better model

7. **Compare Results & Select Best Model**

---

## 🏆 Results Summary

| Model | MSE |
|------|------|
| Mean Baseline | 1425.724284 |
| Linear Regression | 51.655421 |
| Polynomial Degree 2 | 0.253348 |
| Polynomial Degree 3 | 0.253747 |
| **Polynomial Degree 4** | **0.252353** ✅ |
| Ridge Regression | 51.663215 |
| KNN (k=3) | 1.180265 |
| KNN (k=5) | 1.131587 |
| KNN (k=7) | 1.174846 |
| Weighted Linear Regression | 51.655421 |

---

## 🥇 Best Model

> ✅ **Polynomial Regression (Degree 4)**  
It achieved the **lowest MSE (≈ 0.252353)**, making it the **best-performing model** for this simulation dataset.

---

## 🖼️ Result Screenshot

Add your result image in the repository (for example inside a folder called `images/`) and link it here:

```markdown
<img width="457" height="307" alt="image" src="https://github.com/user-attachments/assets/0a010a34-3c62-43f3-8f46-0043a4cc2184" />

