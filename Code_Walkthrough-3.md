# Code Walkthrough: Protein-Excipients Interaction Prediction

This walkthrough explains the steps used in the `protein_excipients_code.ipynb` notebook, which aims to predict pChEMBL values for excipients interacting with the GLP-1 receptor using machine learning.

## 1. Library Imports

The script begins by importing necessary libraries:
- `pandas`, `numpy`: for data handling
- `matplotlib.pyplot`, `seaborn`: for visualisation
- `sklearn`: for model building and evaluation
- `rdkit`: for generating molecular fingerprints

## 2. Data Loading

- A dataset of molecules is loaded from a CSV file.
- It includes **SMILES strings** and corresponding **pChEMBL values**, which measure biological activity.

## 3. Feature Engineering

- Molecules are converted into **Morgan fingerprints** using RDKit.
- These binary fingerprints capture molecular structure and are used as input features for the models.

## 4. Model Building

Three regression models are trained:
- **Random Forest Regressor**
- **Support Vector Regressor (SVR)**
- **Multi-Layer Perceptron Regressor (MLP)**

The dataset is split into training and test sets before training each model.

## 5. Model Evaluation

Each model is evaluated using:
- **R² (coefficient of determination)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**

The models are compared based on their performance in predicting pChEMBL values.

## 6. Prediction on Excipients

- A separate list of **excipients** (non-active ingredients in drugs) is loaded.
- SMILES for excipients are converted to Morgan fingerprints.
- The trained model is used to **predict pChEMBL values** for these compounds.
- Results are sorted to highlight excipients with potentially high interaction with GLP-1.

## 7. Visualisation

- Bar plots are used to visualise the predicted pChEMBL values of the top excipients.

## Conclusion

The notebook builds and evaluates machine learning models to predict molecular interactions and applies them to screen excipients. This workflow can help prioritise excipients with potential bioactivity at the GLP-1 receptor.
