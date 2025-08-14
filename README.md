# Blood Donation Analysis — Statistical Tests & Data Exploration

## Overview
This repository contains a Jupyter Notebook that analyzes blood donation patterns across different blood types and Malaysian states.  
The project applies statistical hypothesis testing, correlation analysis, and principal component analysis (PCA) to evaluate relationships between blood types and determine whether a composite index can be constructed.

---

## Dataset Sources
The data used in this analysis comes from the **Department of Statistics Malaysia**:

- [Population Malaysia Dataset](https://data.gov.my/data-catalogue/population_malaysia)  
- [Blood Donations by State Dataset](https://data.gov.my/data-catalogue/blood_donations_state)  

Please cite these datasets appropriately when reusing this analysis.

---

## Key Analyses
The notebook performs the following steps:

### 1. Data Preparation & Cleaning
- Load population and blood donation datasets.
- Merge and reshape into an analysis-ready format.
- Handle missing values and outliers.

### 2. Exploratory Data Analysis (EDA)
- Summary statistics and data visualizations.
- Distribution checks and correlation matrices.

### 3. Statistical Tests
- **Chi-squared tests** for goodness of fit.
- **Kruskal–Wallis test** for comparing distributions.
- **Bonferroni correction** for multiple testing adjustments.
- **Kendall’s τ correlation** for donation time series across blood types.

### 4. Dimensionality Reduction
- **Principal Component Analysis (PCA)** with robust centering and scaling.
- Evaluate proportion of variance explained by PC1 and uniformity of loadings.

### 5. Agreement Assessment
- **Intraclass Correlation Coefficient (ICC, model 3k)** to measure agreement between blood types over time.

### 6. Aggregation Criteria
- Mean Kendall’s τ ≥ 0.60  
- PC1 variance explained ≥ 90%  
- Consistent PC1 loadings  
- Robust ICC(3k) ≥ 0.90  

---

## Requirements
The analysis was developed in Python 3.  
Key dependencies are listed in `requirements.txt`.

Install all dependencies:
```bash
pip install -r requirements.txt
```

---

## Usage
Clone the repository:
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

Open the notebook in Jupyter or Google Colab:
```bash
jupyter notebook blood_donation_analysis.ipynb
```

Run all cells to reproduce the analysis.

---

## Citation
If you use this repository, please cite the relevant statistical methods and data sources:

- Department of Statistics Malaysia. (2024). *Population Malaysia Dataset*.  
- Department of Statistics Malaysia. (2024). *Blood Donations by State Dataset*.  
- Koo, T. K., & Li, M. Y. (2016). *A Guideline of Selecting and Reporting Intraclass Correlation Coefficients for Reliability Research*. Journal of Chiropractic Medicine, 15(2), 155–163. https://doi.org/10.1016/j.jcm.2016.02.012  
- Maćkiewicz, A., & Ratajczak, W. (1993). *Principal components analysis (PCA)*. Computers & Geosciences, 19(3), 303–342.  
