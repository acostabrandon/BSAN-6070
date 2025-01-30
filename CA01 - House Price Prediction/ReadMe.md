# CA-01 Housing Predictions

## Assignment Overview
This project is part of BSAN 6070 - Intro to Machine Learning and focuses on house price prediction datafile through exploratory data analysis (EDA) and data cleaning through the use of a data quality report.

## Technologies & Packages Used
This analysis was conducted using **Python** in a Jupyter Notebook environment. The following libraries were used:
- `pandas` - Data manipulation and cleaning
- `numpy` - Numerical computations
- `matplotlib` - Data visualization
- `seaborn` - Statistical visualizations

## Steps in the Analysis
### **1: Data Understanding & Exploratory Data Analysis (EDA)**
- Visualized distributions of numerical & categorical features using histograms, boxplots, countplots, and scatterplots.
- Examined missing values and patterns in the dataset.
- Generated a correlation heatmap to identify relationships between variables.
- Conducted outlier analysis using the IQR method.

### **2: Data Preprocessing**
- **Handled missing values:**
  - Categorical missing values filled with `'None'`.
  - Numerical missing values imputed using the median.
- **Addressed outliers:**
  - Identified extreme values for variables such as `LotFrontage`, `GrLivArea`, `GarageArea`, and `SalePrice`.
  - Considered removal or transformation of extreme outliers.
- **Feature Engineering:**
  - Created bins for `YearBuilt` to group houses by age.
  - Applied log transformation to `SalePrice` and other skewed features to normalize distributions.

## Key Insights
- OverallQual and GrLivArea are the strongest predictors of `SalePrice`.
- Outliers in LotArea and SalePrice significantly impacted data distribution.
- Most categorical features had dominant categories, which may influence predictive modeling.

## Data Used for Insights
- Data was accessed through the following GitHub link from Professor Brahma's files: https://github.com/ArinB/MSBA-CA-Data/raw/refs/heads/main/CA01/house-price-train.csv
---
For any questions or feedback, feel free to reach out!

