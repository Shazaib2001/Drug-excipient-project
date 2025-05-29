# Protein-Excipients Interaction Prediction using Machine Learning

## Project Overview

This project applies machine learning to predict the interaction strength between pharmaceutical excipients and the GLP-1 receptor using pChEMBL values. By training regression models on known molecule-receptor interactions, the analysis estimates which commonly used excipients might exhibit off-target biological effects, contributing to early safety screening in drug development.

## Data Source and Description

The dataset contains molecules represented by SMILES strings along with their experimentally measured pChEMBL values for GLP-1 receptor binding. A secondary dataset contains excipients with corresponding SMILES strings. Molecular fingerprints (Morgan fingerprints) are generated to represent molecular structures numerically.

## Analysis Techniques

- **Molecular Fingerprints**: RDKit is used to generate Morgan fingerprints from SMILES strings.
- **Machine Learning Models**:
  - Random Forest Regressor
  - Support Vector Regressor (SVR)
  - Multi-Layer Perceptron (MLP)
- **Evaluation Metrics**:
  - R² Score
  - RMSE
  - MAE

## Results

- The Random Forest model achieved the best performance based on R² and error metrics.
- Predictions on excipients revealed several compounds with potentially high pChEMBL scores, suggesting possible unintended activity at the GLP-1 receptor.
- Visualisation helped rank top excipients by predicted bioactivity.

## Installation

Install required libraries using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn rdkit
```

## Usage

1. Load the notebook `protein_excipients_code.ipynb`.
2. Run all cells to train models and predict pChEMBL values for excipients.
3. Review plots and output to identify top candidate excipients.

## Contributing

Contributions are welcome. Fork the repository and submit a pull request for enhancements or fixes.

## License

This project is licensed under the MIT License.

## Contact

For queries, please contact **Shazaib Rehman**.  
Connect with me on [LinkedIn](https://www.linkedin.com).
