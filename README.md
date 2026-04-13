# Ensemble QSAR Model for GSK3β Inhibitor Prediction

PLIP-based target-specific descriptor generation + 5-stage ensemble QSAR pipeline  
for predicting GSK3β inhibitor activity.

## Pipeline Overview

| Stage | File | Description |
|-------|------|-------------|
| 1 | `base_model_(abl).py` | Baseline model with ablation study |
| 2 | `feature_selection_model(abl).py` | Feature group selection |
| 3 | `mrmr_model(abl).py` | mRMR-based feature selection |
| 4 | `mrmr+gaussian_process_regressor_model(abl).py` | mRMR + GPR ensemble |
| 5 | `final_gsk3β_optimum.py` | Final optimized ensemble model |

## Key Features
- PLIP-based protein-ligand interaction descriptor generation
- Target-specific descriptor validated via SHAP analysis
- Ensemble stacking: RF, GBM, SVR, GPR (7 algorithms)
- Bayesian-optimized hyperparameters

## Performance (Test Set)
- R² = 0.65
- AUC-ROC = 0.869
- Classification accuracy = 73%

## Tools & Libraries
RDKit, Mordred, scikit-learn, SHAP, PLIP, ChEMBL API, BayesianOptimization
