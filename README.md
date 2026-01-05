# Modeling CO₂ Emissions Using Economic and Energy Indicators

## Project Overview
This project analyzes country level **CO₂ emissions per capita** and their relationship with key economic and energy use variables using modern statistical and machine learning methods. The primary objective is to understand the drivers of CO₂ emissions and to compare interpretable and predictive modeling approaches.

The project was completed as part of a graduate level statistical computing course and received a **perfect score**.

---

## Research Questions
- How do energy consumption and economic factors influence CO₂ emissions per capita?
- Can CO₂ emissions per capita be accurately predicted using a small, interpretable set of variables?
- How do linear penalized regression models compare to nonlinear machine learning models in predictive performance?

---

## Data Description
The data come from the **Our World in Data CO₂ and Greenhouse Gas Emissions** dataset.

- **Original dataset:**  
  - 25,204 observations  
  - 58 variables  
- **Cleaned dataset (used for modeling):**  
  - 2,299 observations  
  - 11 variables  
  - Years ≥ 1990  
  - Complete case observations only  

Key variables include:
- CO₂ emissions per capita (response variable)
- GDP
- Population
- Coal, oil, and gas CO₂ emissions
- Energy consumption measures

---

## Methods
The analysis follows four main stages:

1. **Exploratory Data Analysis (EDA)**  
   - Examination of skewness, missingness, and correlations  
   - Visualization of raw and transformed variables  

2. **Data Transformation**  
   - Log transformations applied to reduce skewness and improve interpretability  
   - Resulting coefficients are interpretable as elasticities  

3. **Modeling Approaches**
   - **Ridge Regression (Interpretable Model)**  
     - Handles multicollinearity using an ℓ₂ penalty  
     - Penalty parameter selected using **10-fold cross-validation**
   - **Random Forest (Predictive Model)**  
     - Captures nonlinear relationships and interactions  
     - Tuned using **10-fold cross-validation**  
     - Final model used 500 trees, `mtry = 3`, and node size = 5  

4. **Model Evaluation**
   - Performance assessed using **RMSE** and **MAE** on an independent test set  

---

## Results Summary
- **Random Forest** achieved substantially lower RMSE and MAE, indicating superior predictive performance.
- **Ridge Regression** provided stable, interpretable coefficient estimates and insight into how energy and economic variables affect CO₂ emissions.
- Energy use per capita and fossil fuel emissions (coal, oil, gas) were consistently identified as the most influential predictors.

---

## Files in This Repository
- `Rahmat_Final_Project.Rmd` – Fully reproducible R Markdown file  
- `Rahmat_Final_Project.pdf` – Final submitted report (no code, clean output)   
- `README.md` – Project overview and documentation  

---

## How to Reproduce
1. Clone this repository.
2. Open `Rahmat_Final_Project.Rmd` in RStudio.
3. Install required R packages listed at the top of the file.
4. Knit the R Markdown file to PDF.

All modeling steps, cross-validation, and visualizations are fully reproducible.

---

## Notes
- The PDF report intentionally excludes R code and console output to emphasize interpretation and results.
- All code used for analysis is contained in the R Markdown file and Appendix.
- This project demonstrates both **statistical modeling** and **machine learning** approaches applied to an environmental dataset.

---

## Author
**Rahmat Adepo**  
M.S. Statistics  
BSc. Surveying and Geoinformatics

