# Electric Scooter Market Analysis — Brazil

## Overview

This project analyzes the growth of the electric scooter market in Brazil and identifies the key factors that explain and anticipate this expansion.

The work is structured as a full data science pipeline, combining data engineering, exploratory analysis, feature engineering, and business interpretation.

The goal is not only to describe market growth, but to understand **where opportunities are concentrated and which signals can anticipate demand**.

---

## Central Question

**Which factors explain and help anticipate the growth of the electric scooter market in Brazil?**

---

## Methodological Approach

The analysis is intentionally split into two complementary perspectives:

- **Observed national demand**  
  Based on imports and Google Trends over time  

- **State-level opportunity**  
  Based on GDP, population, and two-wheel fleet  

This separation is necessary because the dataset does **not include observed scooter adoption by state**.

Whenever a question cannot be answered directly from the data, I explicitly acknowledge this instead of forcing unsupported conclusions.

---

## Tech Stack & Methods

###  Tools & Libraries

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  
- Scikit-learn  

###  Analytical Techniques

- Data cleaning and standardization  
- Exploratory Data Analysis (EDA)  
- Feature engineering  
- Time series analysis (lags and leading indicators)  
- Correlation analysis  
- Clustering (unsupervised learning for market segmentation)  
- Regression modeling (with explicit limitations)  

---

## Data Sources

The project integrates multiple raw sources:

- Import data (COMEX)  
- Google Trends  
- GDP (IBGE)  
- Population data  
- Two-wheel vehicle fleet  

All data is loaded from a structured local `DATA/` directory to ensure reproducibility.

---

## Key Features Engineered

- Growth (year-over-year imports)  
- Average import price per unit  
- GDP per capita  
- Fleet per capita (two-wheel vehicles)  
- Lagged Google Trends indicators (3 and 6 months)  

Because state-level scooter consumption is not available, the project builds a **transparent proxy** instead of using misleading assumptions.

---

## Main Findings

### Market Growth

- Imports increased from **96,242 units (2020)** to **1,358,284 units (2025)**  
- This represents a **~14x market expansion**  
- Estimated CAGR: **~69.8% per year**

---

### Leading Indicator

- **Google Trends** is the strongest observable leading signal  
- Lagged search interest (3–6 months) shows strong correlation with future demand  

---

### Pricing Dynamics

- Falling average import price per unit is consistent with:
  - market expansion  
  - increased accessibility  

---

### Regional Opportunity

Market potential is not evenly distributed:

- **Southeast** → strongest purchasing power and scale  
- **Center-West** → highest mobility intensity per capita  
- **Northeast** → large two-wheel base and emerging demand  

---

### State-Level Insights (Proxy-Based)

Top opportunity states:

- São Paulo  
- Mato Grosso  
- Minas Gerais  
- Rio de Janeiro  
- Paraná  

These reflect a mix of:

- large-scale markets  
- high-intensity mobility markets  

---

## Clustering Insights

Three distinct market profiles emerge:

- **High potential** → São Paulo (scale outlier)  
- **Consolidated markets** → large, wealthier regions with strong mobility  
- **Emerging markets** → smaller but high-intensity regions with growth potential  

---

## Modeling Limitations

A regression model was implemented using:

- GDP per capita  
- fleet per capita  
- lagged trends  

However:

- Only **2 aligned observations** were available  
- This is **not sufficient for statistical validity**

I explicitly report this limitation instead of presenting unreliable results.

---

## Hypothesis Validation

- Strongest support found for:
  - **Digital interest preceding demand (H1)**  

- Not fully testable:
  - GDP → adoption  
  - fleet → adoption  
  - relative growth patterns  

**Reason:** lack of state-level adoption data

---

## Key Takeaways

- The electric scooter market in Brazil is **growing rapidly**  
- Growth accelerated significantly after 2023  
- **Digital behavior (search interest)** is the most useful predictive signal  
- Market opportunity is driven by a combination of:
  - economic capacity  
  - mobility culture  

---

## Final Note

I intentionally kept this project honest. The analysis is strong and consistent, but limited by the available data. A reliable state-level adoption dataset would immediately upgrade this work from opportunity mapping to true explanatory and predictive modeling.



