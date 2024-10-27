# README for a DN Prediction Stacking Model
> This is the ML source code for the donor number (DN) prediction model, developed for the research article titled "Machine Learning Assisted Prediction of Donor Numbers: Guiding Rational Fabrication of Polymer Electrolytes for Lithium-ion Batteries."
>
> The code has been organized into distinct sections, each focusing on a specific phase of the modeling process, such as data preparation, model training, evaluation, and prediction.

## Prerequisites

To execute the code successfully, ensure you have the following prerequisites in place:

- Anaconda: A distribution of Python and R for scientific computing, which comes with a collection of pre-installed data science libraries.
- PyCharm: An Integrated Development Environment (IDE) for professional developers, which provides smart coding assistance and a seamless experience for Jupyter Notebooks.
- Jupyter Notebook: An open-source web application that allows you to create and share documents containing live code, equations, visualizations, and narrative text.
- Necessary Python libraries: numpy, pandas, matplotlib, seaborn, scikit-learn, xgboost, shap.

You can install the required libraries using Anaconda or pip:

```bash
conda install numpy pandas matplotlib seaborn scikit-learn xgboost shap
```

or

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost shap
```

## Data

* The dataset used for training and evaluating the model is an Excel file named `dataset.xlsx`. This file contain the target variable (DN value) in the 2nd column and the corresponding features in the other columns.
* The Excel file named `data_to_be_predicted.xlsx` contain the corresponding features of the material to be predicted.
* The CSV file named `selected_feats.csv` and `selected_features.csv` list the selected features for modeling.

## Installation

* If Jupyter Notebook is not installed in your environment, you can install it with the following command:
```python
pip install jupyter
```
* 


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



# README for Stacking Model


## Data

The dataset used for training and evaluating the model is expected to be in an Excel file named `dataset.xlsx`. This file should contain the target variable in one column and the corresponding features in the other columns. Additionally, a CSV file named `selected_feats.csv` should list the selected features for modeling.

## Code Structure

The code is structured into several sections for clarity and modularity:

1. **Multiple Regression Model Predictions**
   - Imports necessary libraries and modules.
   - Loads the dataset, handling missing values as needed.
   - Defines a function to generate non-consecutive combinations for feature selection.

2. **Data Selection**
   - Splits the dataset into features (X) and the target variable (y).
   - Implements functions for K-Fold cross-validation and model evaluation metrics.

3. **Multi-regression Evaluation**
   - Establishes a dictionary of base models with their respective hyperparameter grids.
   - Conducts cross-validation, grid search for hyperparameter tuning, and evaluates model performance.

4. **Stacking Model**
   - Configures the base models and the meta-model within the stacking framework.
   - Performs cross-validation and assesses the stacked model's performance.

5. **Metrics**
   - Computes and records the model's performance metrics, such as R2, MAE, and RMSE.

6. **SHAP Values**
   - Calculates and visualizes the SHAP values for the base models to understand feature importance.

7. **Stacking Prediction**
   - Prepares the data for predictions, standardizing features as necessary.
   - Defines and trains the stacking model on the prepared data.
   - Generates predictions and saves the model and prediction results to files.

## Running the Code

To run the code effectively:

1. Install Anaconda and set up a new environment with the required libraries.
2. Open PyCharm and create a new project in your desired directory.
3. Install the Jupyter Notebook plugin in PyCharm if not already installed.
4. Import the `dataset.xlsx` and `selected_feats.csv` files into the project directory.
5. Open the Jupyter Notebook in PyCharm and run each cell sequentially.
6. The final model predictions will be saved to a CSV file named `selected_prediction.csv`.

## Model Performance

The model's performance is evaluated using key metrics, including R2, MAE, and RMSE, with the results being saved to a CSV file named `best_results_r2_mae_rmse.csv`.

## SHAP Values

SHAP values are calculated for each feature, providing insights into their individual contributions to the model's predictions. These values are visualized using swarm plots and saved as PDF files for further analysis.

## Predictions

The stacking model is utilized to make predictions on new, unseen data. The predictions are stored in a CSV file named `selected_prediction.csv`.

## Note

While this README provides a high-level overview and instructions, it is crucial to review and understand the code in each section before execution. The recommendation to use Jupyter Notebook in Anaconda with PyCharm software is to ensure a smooth development environment and efficient coding assistance.

