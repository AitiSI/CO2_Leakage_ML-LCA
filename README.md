![image](https://github.com/AitiSI/CO2_Leakage_ML-LCA/blob/main/CURE_logo_2.png)

# Machine Learning and Climate Impact Assessment for CO₂ Leakage in Geological Carbon Storage
---
This repository contains the Python workflow used to develop machine learning surrogate models for predicting CO₂ leakage through adjacent wells and evaluating climate impact metrics in geological carbon storage systems.

The models are trained using reservoir simulation datasets and are designed to estimate storage performance, leakage behavior, and environmental implications associated with CO₂ storage operations.

### Authors: Sanchez Aitiana; Honggeun Jo
### Affiliation: [INHA_ERE](https://eneres.inha.ac.kr/eneres/index.do), [CURESAL_lab](https://petroinha.github.io/)

## Running the Code

To get started, run the scripts located in the scripts directory.
These scripts reproduce the machine learning workflow used in the study, including:

1. Data preparation and preprocessing
2. Training of machine learning models (ANN and Random Forest)
3. Model validation and performance evaluation
4. Feature importance analysis
5. Generation of figures and visualization of results
6. Calculation of climate impact metrics (LCA-based indicators)

### Example workflow:

- python train_ANN.py
- python train_RF.py
- python feature_importance.py
- python plots.py

### Required Python libraries can be installed using:
- pip install -r requirements.txt

## Repository Contents

- data_example/example_dataset.csv: Example dataset demonstrating the structure of the simulation results used to train the machine learning models.
- scripts/train_RF.py: Script used to train Random Forest (classification) models and evaluate predictive performance.
- scripts/train_ANN.py: Script used to train Artificial Neural Network (ANN) (regression) models for predicting CO₂ storage and leakage outcomes.
- scripts/feature_importance.py: Computes global feature importance to identify key parameters controlling leakage behavior.
- scripts/plots.py: Generates visualization figures such as parity plots and model evaluation plots.
- figures/ :Example output figures produced by the analysis scripts.
- requirements.txt: List of Python packages required to run the workflow.

## LICENSE
MIT License allowing reuse and adaptation of the code.

## Data Availability

The repository includes a small example dataset to demonstrate the workflow.

The complete simulation dataset used in this research is not publicly available.

## Research Context

This repository supports research focused on:
- CO₂ leakage through adjacent wells
- Machine learning surrogate modeling for reservoir simulations
- Evaluation of climate impact metrics associated with CO₂ storage performance
- Risk assessment for geological carbon storage systems

The workflow combines reservoir engineering simulations with machine learning techniques to improve computational efficiency and enable rapid analysis of large parameter spaces.

## Citation

A publication associated with this repository is currently in preparation.
Citation information will be added once the article is published.

## Questions or Feedback

If you have any questions regarding this repository or the workflow, please contact:
Please reach out to a.sanchezismodes23@inha.edu or honggeun.jo@inha.ac.kr.
