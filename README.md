# Probability Density Function Estimation using Roll-Number-Parameterized Non-Linear Model

## Assignment Overview
This repository contains the solution for **Assignment 1**, which focuses on learning a probability density function (PDF) after applying a **roll-number-dependent non-linear transformation** to real-world air quality data.

The dataset used is the **India Air Quality Dataset (Kaggle)**, and **NO₂ concentration** is considered as the input feature.

---

## Dataset
- **Source:** https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data
- **Feature used:** `NO2`
- Missing and non-numeric values are handled during preprocessing.

---

## Roll Number 102303744


---

## Step 1: Non-Linear Transformation

Each value of NO₂ (denoted as `x`) is transformed using the function:

\[
z = x + a_r \sin(b_r x)
\]

Where:
- \( a_r = 0.05 \times (r \bmod 7) = 0.2 \)
- \( b_r = 0.3 \times (r \bmod 5 + 1) = 1.5 \)
- \( r \) is the university roll number

---

## Step 2: Probability Density Function Learning

The transformed variable `z` is modeled using the following PDF:

\[
\hat{p}(z) = c \cdot e^{-\lambda (z - \mu)^2}
\]

### Parameter Estimation Method
- Parameters are estimated using **Maximum Likelihood Estimation (MLE)**
- Mean and variance are computed directly from transformed data

Formulas used:
- \( \mu = \mathbb{E}[z] \)
- \( \lambda = \frac{1}{2\sigma^2} \)
- \( c = \sqrt{\frac{\lambda}{\pi}} \)

---

## Final Estimated Parameters

| Parameter | Value |
|--------|--------|
| **μ (mean)** | 25.81637541398808 |
| **λ (lambda)** | 0.001461472898753684 |
| **c (normalization constant)** | 0.02156852503216156 |

These are the values submitted for evaluation.

---

## Technologies Used
- Python 3
- NumPy
- Pandas
- Math library

---

## How to Run
1. Clone the repository
2. Place `data.csv` in the project directory
3. Run the Jupyter Notebook or Python script
4. The estimated parameters will be printed in the output

---

**Aishita Kumar**  
Roll No: 102303744

---


