# ADMET Isostere Classification

This repository contains the final analysis pipeline, dataset, thesis materials, and selected results prepared as part of a bachelor's thesis project.

The project focuses on drug class prediction and bioisostere generation using molecular fingerprints, RDKit descriptors, machine learning classifiers, and dynamic classifier selection methods.

## Thesis Context

This repository was created to organize and document the computational part of my bachelor's thesis. The goal of the project is to investigate whether generated bioisosteric analogues of known drug molecules preserve the predicted therapeutic class of the original compounds.

The main workflow is kept in a single Jupyter notebook to make the analysis easy to follow from data loading to model evaluation and interpretation.

## Repository Structure

```text
.
├── data/
│   └── all_chem_df.csv
├── notebooks/
│   └── pipeline_notebook.ipynb
├── results/
│   ├── figures/
│   └── reports/
├── models/
├── .gitignore
└── README.md
```

## Main Files

- `notebooks/pipeline_notebook.ipynb` - final end-to-end analysis pipeline.
- `data/all_chem_df.csv` - main dataset used in the project.
- `results/figures/` - exported figures and molecular visualizations.
- `results/reports/` - exported result tables, model metrics, and rankings.
- `models/` - local model cache directory. Large generated model files are excluded from version control.

## Methods

The pipeline includes:

- molecular preprocessing with RDKit
- Morgan fingerprint generation
- calculation of selected RDKit molecular descriptors
- bioisostere generation using reaction SMARTS
- scaffold-based train/test splitting
- drug class prediction using machine learning classifiers
- model evaluation with accuracy, balanced accuracy, and macro F1-score
- dynamic classifier selection with DESlib
- feature importance analysis and molecular interpretability visualization

## Models

The project compares several classification approaches:

- Random Forest
- Support Vector Machine
- Logistic Regression
- XGBoost
- DESlib-based dynamic classifier selection methods

## Results

The final notebook produces model evaluation metrics, descriptor comparisons between original molecules and generated bioisosteres, and rankings of generated analogues according to predicted class preservation.

Generated result files should be stored in:

- `results/reports/` for tables, metrics, and rankings
- `results/figures/` for molecular visualizations and exported figures

## Requirements

The analysis was developed in Python using Jupyter Notebook. Main libraries include:

- pandas
- numpy
- scikit-learn
- xgboost
- RDKit
- DESlib

## Notes

Large model cache files are not tracked in Git. If cache files are missing, the notebook can retrain the models.

Dataset licensing may depend on the original data sources.

## Author

Franciszek Karpinski
