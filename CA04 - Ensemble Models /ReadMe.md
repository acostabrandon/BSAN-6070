# CA04: Ensemble Models for Salary Prediction

## Project Overview
This project is part of the Machine Learning course and focuses on building and evaluating ensemble models to predict salary categories ('>50K' and '<=50K') based on demographic features. The objective is to compare the performance of different ensemble models using accuracy and AUC as evaluation metrics.

## Dataset Description
The dataset is obtained from the Census Bureau and represents salaries of individuals along with seven demographic variables.

- Number of Target Classes: 2 ('>50K' and '<=50K') [Labels: 1, 0]
- Number of Attributes (Columns): 7
- Number of Instances (Rows): 48,842
- Data Source:
  https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true

The dataset includes a column indicating whether a row belongs to the training or testing dataset.

## Necessary Packages and Libraries
To successfully run the notebook, make sure you have the following libraries installed:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

You can install the necessary libraries using pip:
```
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

## Methodology and Steps
1. Data Loading and Preparation:
   - Load the data from the specified URL.
   - Split the data into training and testing sets based on the 'flag' column.
   - Preprocess data as needed (no additional cleaning required since it was previously processed in CA03).

2. Model Building and Evaluation:
   - Implemented four ensemble models:
     - Random Forest
     - AdaBoost
     - Gradient Boosting
     - XGBoost
   - Evaluated each model by tuning the hyperparameter `n_estimators` in the range [50, 100, 150, ..., 500].

3. Hyperparameter Tuning:
   - Found the optimal value of `n_estimators` by plotting:
     - Accuracy vs. n_estimators
     - AUC vs. n_estimators

4. Performance Comparison:
   - Created a comparison table to summarize the optimal number of estimators for each model based on accuracy and AUC.

## How to Run the Notebook
1. Clone the repository:
   git clone https://github.com/username/ensemble-models-ca04.git

2. Open the Jupyter Notebook:
   jupyter notebook ca_04_ensemble_model.ipynb

3. Execute the cells to train models and visualize results.
