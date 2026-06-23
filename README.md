# ADMET Isostere Classification

This repository contains the final analysis pipeline, dataset, thesis materials, and selected results prepared as part of a bachelor's thesis project @ Jagiellonian University, Kraków.

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
│   └── pipeline_notebook.ipynb - final end-to-end analysis pipeline.
├── results/
│   ├── figures/ - exported figures and molecular visualizations.
│   └── reports/ - exported result tables, model metrics, and rankings.
├── models/ - local model cache directory. Large generated model files are excluded from version control.
├── .gitignore
└── README.md
```

## Methods

The pipeline includes:

- molecular preprocessing with RDKit
- bioisostere generation using reaction SMARTS
- drug class prediction using machine learning classifiers
- model evaluation, dynamic classifier selection with DESlib
- feature importance analysis and molecular interpretability visualization

## Results

The final notebook produces model evaluation metrics, descriptor comparisons between original molecules and generated bioisosteres, and rankings of generated analogues according to predicted class preservation.

## Notes

Large model cache files are not tracked in Git. If cache files are missing, the notebook can retrain the models.

Dataset licensing may depend on the original data sources.

## Author

Franciszek Karpinski
