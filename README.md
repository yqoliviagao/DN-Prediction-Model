# README for a DN Prediction Stacking Model
> This is the ML source code for the donor number (DN) prediction model, developed for the research article titled "Machine Learning Assisted Prediction of Donor Numbers: Guiding Rational Fabrication of Polymer Electrolytes for Lithium-ion Batteries."
> 

## Prerequisites

Before running the code, ensure you have the following libraries installed:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- xgboost
- shap

You can install these libraries using pip:

```python
pip install numpy pandas matplotlib seaborn scikit-learn xgboost shap
```

## Installation

* If Jupyter Notebook is not installed in your environment, you can install it with the following command:
```python
pip install jupyter
```
* Make sure that the following mandatory libraries are installed in your environment. If they are not installed, you can use the pip command to install them:
```python
pip install numpy pandas matplotlib seaborn scikit-learn xgboost
```

## Usage

1. Open a terminal or command prompt.
2. Navigate to the directory containing “Stacking_model.ipynb”.
3. Run the following command to start the Jupyter Notebook server:
```python
jupyter notebook
```
5. In the Jupyter Notebook interface, locate and open the “Stacking_model.ipynb” file.
6. Run each cell one by one, following the order of the cells in the Notebook. You can execute the code by clicking the Run button to the left of each cell.
7. View the output of each cell to see how the model is running and performing.


**Note**: 
* Make sure you have installed all the necessary libraries before running the code.
* If you encounter any problems during runtime, check that the versions of the code and libraries are compatible.
* Running the model may require some computing resources, make sure your device meets the running requirements.


```python

```

# Description of the code structure
## 1. Multiple regression model predictions: 
  This part of the code contains predictions from multiple regression models.
## 2. Stacking Model: 
  This part of the code implements a stacking model to improve the accuracy of the predictions.


# Version Information
 Jupyter Notebook version: [7.0.8]
 
 Python version: [3.12.2]

# Contribute 







## Data

The data used for training and testing the model is assumed to be in an Excel file named `dataset.xlsx`. The file should have the training set values in one column and the corresponding features in the remaining columns. Additionally, a CSV file named `selected_feats.csv` should contain the list of selected features.

## Code Structure

The code is divided into several sections:

1. **Multiple Regression Model Predictions**
   - Imports necessary libraries.
   - Loads the dataset and fills missing values.
   - Defines a function to generate non-consecutive combinations.
   - Selects the features based on the `selected_feats.csv` file.

2. **Data Selection**
   - Splits the data into features (X) and target variable (y).
   - Defines functions for cross-validation and model evaluation.

3. **Multi-regression Evaluation**
   - Defines a dictionary of base models and their parameters.
   - Performs cross-validation and grid search for hyperparameter tuning.

4. **Stacking Model**
   - Defines the base models and the meta-model for the stacking approach.
   - Performs cross-validation and evaluates the model's performance.

5. **Metrics**
   - Calculates the model's performance metrics such as R2, MAE, and RMSE.

6. **SHAP Values**
   - Calculates the SHAP values for the base models and visualizes them.

7. **Stacking Prediction**
   - Loads the data to be predicted.
   - Standardizes the features.
   - Defines the stacking model and trains it on the data.
   - Makes predictions and saves the model and predictions to files.

## Running the Code

To run the code, follow these steps:

1. Place the `dataset.xlsx` and `selected_feats.csv` files in the same directory as the Jupyter notebook.
2. Run each cell in the notebook sequentially.
3. The final predictions will be saved to a CSV file named `selected_prediction.csv`.

## Model Performance

The model's performance is evaluated using various metrics, including R2, MAE, and RMSE. The results are saved to a CSV file named `best_results_r2_mae_rmse.csv`.

## SHAP Values

The SHAP values are calculated for each feature and visualized using a swarm plot. The plots are saved as PDF files.

## Predictions

The stacking model is used to make predictions on new data. The predictions are saved to a CSV file named `selected_prediction.csv`.

## Disclaimer

This README file is generated based on the provided code and may not cover all the details. It is essential to review the code and understand each section's purpose before running it.

