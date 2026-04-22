# 🛢️ Oil Investment Optimization | Optimización de Inversión Petrolera

## 🇺🇸 English

### 📌 Project Overview

Making investment decisions in the oil industry involves significant uncertainty and financial risk.

This project develops a **data-driven decision framework** to identify the most profitable region for drilling oil wells, combining machine learning predictions with statistical simulation techniques.

---

### 🎯 Business Problem

The company OilyGiant needs to decide:

> Where to invest **$100 million** to develop **200 oil wells** while minimizing financial risk.

---

### 🎯 Objective

* Predict oil reserves using machine learning
* Select the top 200 wells per region
* Estimate potential profit
* Evaluate **risk of loss (< 2.5%)** using bootstrapping

---

### 📊 Dataset

Three regions with geological exploration data:

* Features: `f0`, `f1`, `f2`
* Target: `product` (thousands of barrels)

---

### ⚙️ Methodology

#### 1. Data Preparation

* Removed missing values
* Split data (75% train / 25% validation)

#### 2. Modeling

* Model used: **Linear Regression**
* Evaluation metric: **RMSE**

#### 3. Business Logic

* Budget: **$100M**
* Revenue per unit: **$4,500**
* Minimum viable production: **111.1 units per well**

#### 4. Profit Calculation

* Selected **top 200 wells** based on predictions
* Estimated total revenue and profit

#### 5. Risk Analysis (Key Step 🚀)

* Applied **Bootstrapping (1000 simulations)**
* Calculated:

  * Mean profit
  * 95% confidence interval
  * Probability of loss

---

### 📈 Results

| Region   | RMSE  | Avg Prediction | Mean Profit | Risk of Loss |
| -------- | ----- | -------------- | ----------- | ------------ |
| Region 0 | 37.58 | 92.59          | -$17M       | 100%         |
| Region 1 | 0.89  | 68.73          | -$38M       | 100%         |
| Region 2 | 40.03 | 94.97          | -$14M       | 100%         |

---

### ⚠️ Key Insight

Although Region 1 shows the **lowest prediction error**, its oil reserves are insufficient to meet profitability thresholds.

---

### 🚫 Final Decision (Critical Insight)

> ❗ **No region meets the required risk criteria (< 2.5%)**

All regions show:

* Negative expected profit
* 100% probability of loss

---

### 💼 Business Impact

* Prevented a **high-risk $100M investment**
* Demonstrated the importance of combining ML with risk analysis
* Provided a **data-driven rejection strategy**, avoiding financial loss

---

### 🧠 Key Learnings

* Model accuracy ≠ business success
* Risk analysis is essential for decision-making
* Bootstrapping is a powerful tool for uncertainty estimation

---

### 🛠 Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib
* SciPy

---

## 🇲🇽 Español

### 📌 Descripción del Proyecto

La toma de decisiones en la industria petrolera implica alta incertidumbre y riesgo financiero.

Este proyecto desarrolla un **framework de decisión basado en datos** para identificar la región más rentable, combinando Machine Learning con simulación estadística.

---

### 🎯 Problema de negocio

La empresa OilyGiant necesita decidir:

> Dónde invertir **$100 millones** para desarrollar **200 pozos petroleros** minimizando el riesgo.

---

### 🎯 Objetivo

* Predecir reservas de petróleo
* Seleccionar los mejores 200 pozos
* Estimar ganancias
* Evaluar el **riesgo de pérdida (< 2.5%)**

---

### ⚙️ Metodología

#### 1. Preparación de datos

* Eliminación de valores nulos
* División 75/25

#### 2. Modelado

* Regresión Lineal
* Métrica: RMSE

#### 3. Lógica de negocio

* Presupuesto: $100M
* Ingreso por unidad: $4,500
* Umbral mínimo: 111.1 unidades

#### 4. Cálculo de ganancias

* Selección de los 200 mejores pozos
* Estimación de ingresos

#### 5. Análisis de riesgo (CLAVE 🚀)

* Bootstrapping (1000 simulaciones)
* Cálculo de:

  * Ganancia media
  * Intervalo de confianza
  * Probabilidad de pérdida

---

### 📈 Resultados

| Región   | RMSE  | Predicción promedio | Ganancia media | Riesgo |
| -------- | ----- | ------------------- | -------------- | ------ |
| Región 0 | 37.58 | 92.59               | -$17M          | 100%   |
| Región 1 | 0.89  | 68.73               | -$38M          | 100%   |
| Región 2 | 40.03 | 94.97               | -$14M          | 100%   |

---

### 🚫 Decisión final

> ❗ **Ninguna región cumple con el criterio de riesgo**

Todas presentan:

* Ganancias negativas
* 100% probabilidad de pérdida

---

### 💼 Impacto de negocio

* Se evitó una inversión riesgosa de $100M
* Se demostró el valor del análisis de riesgo
* Se proporcionó una recomendación basada en datos

---

### 🧠 Aprendizajes clave

* Un buen modelo no garantiza rentabilidad
* El riesgo es tan importante como la predicción
* Bootstrapping permite tomar decisiones bajo incertidumbre

---

### 🛠 Tecnologías

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib
* SciPy
