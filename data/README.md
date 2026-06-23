# Data Sources

This directory contains the processed dataset used by the final analysis pipeline.

## Main Dataset

- `all_chem_df.csv` - processed molecular dataset used in `notebooks/pipeline_notebook.ipynb`.

The dataset contains SMILES strings and therapeutic class labels used for drug class prediction. The current file has the following columns:

- `image_name` - image filename assigned during dataset preparation
- `tags` - therapeutic class label or labels
- `smiles` - molecular representation in SMILES format
- `Col3` - original label-list representation preserved from the source processing workflow

## Provenance

The final dataset was prepared from PubChem compound identifiers grouped by drug or therapeutic category. Molecular structures were retrieved as isomeric SMILES using PubChemPy, which queries PubChem Compound data.

The preprocessing workflow included:

- retrieving isomeric SMILES for PubChem CIDs
- filtering out very long SMILES strings
- removing salts with RDKit
- deduplicating molecules
- preserving therapeutic class labels as `tags`
- exporting the processed table as `all_chem_df.csv`

The original raw CID text files are not included in this repository. The repository stores the processed dataset used by the final notebook.

## External Resources

- PubChem Compound: https://pubchem.ncbi.nlm.nih.gov/
- PubChemPy: https://pubchempy.readthedocs.io/
- RDKit: https://www.rdkit.org/

## Notes

This dataset is included for reproducibility of the bachelor's thesis analysis. Licensing and reuse conditions may depend on the original data sources.
