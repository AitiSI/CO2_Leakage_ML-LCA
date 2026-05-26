![image](https://github.com/AitiSI/CO2_Leakage_ML-LCA/blob/main/CURE_logo_2.png)

# Machine Learning Screening and GWP100-Based Leakage Assessment for CO₂ Storage

This repository contains the Python workflow used to develop machine learning surrogate models for assessing CO₂ leakage risk through adjacent legacy wells in geological carbon storage systems.

The workflow combines CMG-GEM reservoir simulation outputs, machine learning classification and regression models, sensitivity interpretation, partial dependence analysis, and GWP100-based leakage-penalty metrics. The goal is to support rapid screening of leakage-relevant scenarios and identify physically interpretable controls on stored CO₂ mass, leaked CO₂ mass, and leakage-risk regimes.

## Authors

- Aitiana Sanchez
- Honggeun Jo

**Affiliation:** INHA University, Energy Resources Engineering / CURESAL Lab

---

## Research Context

This repository supports research focused on:

- CO₂ leakage through adjacent legacy wells
- Machine learning surrogate modeling for reservoir simulation datasets
- Random forest classification of leakage-risk regimes
- ANN regression of stored and leaked CO₂ mass
- Feature importance, Morris-like sensitivity screening, and PDP-based interpretation
- GWP100-based CO₂-equivalent leakage penalty assessment
- Decision-oriented screening maps for geological carbon storage

The workflow is intended for preliminary screening within the modeled parameter space and should not be interpreted as a full life-cycle assessment or a regulatory leakage-threshold framework.

---

## Running the Code

To reproduce the workflow, run the scripts located in the `scripts` directory. These scripts cover:

1. Data preparation and preprocessing
2. Leakage-risk classification using Random Forest
3. ANN regression for stored and leaked CO₂ mass
4. Model validation and performance evaluation
5. Feature importance and Morris-like sensitivity screening
6. Partial dependence analysis and LHS-based response diagnostics
7. Generation of figures and decision-oriented maps
8. Calculation of GWP100-based CO₂-equivalent leakage penalties

Required Python libraries can be installed using:
pip install -r requirements.txt

## Repository Contents

- example_dataset.csv: Example dataset demonstrating the structure of the processed simulation results used for model training and analysis.
- train_RF_classification.ipynb: Trains the Random Forest classifier for non-secure leakage-risk regimes and evaluates classification performance.
- train_ANN_regression.ipynb: Trains ANN regression models for predicting stored CO₂ mass and leaked CO₂ mass.
- feature_importance_RF.ipynb: Computes global RF feature importance and class-specific permutation importance to identify key controls on leakage-risk classification.
- ann_sensitivity_analysis.ipynb: Performs Morris-like normalized one-at-a-time sensitivity screening for ANN-predicted stored and leaked CO₂ mass.
- partial_dependence_analysis.ipynb: Generates PDP and LHS-based response diagnostics for interpreting ANN surrogate behavior.
- gwp100_leakage_metrics.ipynb: Computes GWP100-based CO₂-equivalent leakage penalties and retained CO₂-equivalent storage metrics.
- design_maps.ipynb: Generates decision-oriented maps for stored CO₂ mass and leaked CO₂ mass.
- requirements.txt: List of Python packages required to run the workflow.
- LICENSE: MIT License allowing reuse and adaptation of the code.

## LICENSE
MIT License allowing reuse and adaptation of the code.

## Data Availability

This repository includes a small example dataset to demonstrate the workflow and expected data structure.

The complete CMG-GEM simulation dataset and full simulator output files are not publicly included because of file size and software-licensing constraints. Processed input–output data required to reproduce the machine learning analysis may be made available upon reasonable request.

## Notes on Metrics

Stored CO₂ mass and leaked CO₂ mass refer to gas-phase CO₂ inventories extracted from the simulation outputs.

The GWP100-based leakage penalty is calculated from leaked CO₂ mass using a characterization factor of 1 t CO₂-eq per t CO₂. This metric is used as a climate-impact screening indicator and does not represent a full life-cycle assessment.

The retained CO₂-equivalent storage metric is reported as a storage-performance indicator and should not be interpreted as avoided emissions, because no external counterfactual scenario is modeled.

## Citation

A publication associated with this repository is currently in preparation. Citation information will be added once the article is published

## Questions or Feedback

If you have any questions regarding this repository or the workflow,
please reach out to a.sanchezismodes23@inha.edu or honggeun.jo@inha.ac.kr.
