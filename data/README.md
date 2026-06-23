# Data Sources

This directory contains the processed dataset used by the final analysis pipeline.

## Main Dataset

- `all_chem_df.csv` - processed molecular dataset used in `notebooks/pipeline_notebook.ipynb`.

The dataset contains SMILES strings and therapeutic class labels used for drug class prediction. The current file has the following columns:

- `image_name` - image filename assigned during dataset preparation
- `tags` - therapeutic class label or labels
- `smiles` - molecular representation in SMILES format
- `Col3` - original label-list representation preserved from the source processing workflow

## Original Source

The dataset used in this project is based on the dataset described in:

Meyer, J. G., Liu, S., Miller, I. J., Coon, J. J., & Gitter, A. (2019).  
**Learning Drug Functions from Chemical Structures with Convolutional Neural Networks and Random Forests.**  
*Journal of Chemical Information and Modeling*, 59(10), 4438-4449.  
https://doi.org/10.1021/acs.jcim.9b00236

The original dataset contains molecules from PubChem represented as SMILES and annotated with therapeutic function labels based on Medical Subject Headings (MeSH). Molecules may belong to one or more therapeutic classes.

## Dataset Used in This Repository

For this bachelor's thesis project, the dataset was processed and restricted to molecules assigned to a single therapeutic class. This allowed the prediction task to be treated as a single-label multiclass classification problem.

The processed dataset used in the final notebook contains molecules assigned to 12 therapeutic classes.

## Provenance and Preprocessing

The data preparation workflow included:

- reading PubChem compound identifiers grouped by therapeutic category
- removing salts with RDKit
- deduplicating molecules
- preserving therapeutic class labels as `tags`
- filtering the final dataset to single-label molecules during notebook preprocessing

The original raw CID text files are not included in this repository. The repository stores the processed dataset used by the final analysis notebook.

## External Resources

- PubChem Compound: https://pubchem.ncbi.nlm.nih.gov/
- RDKit: https://www.rdkit.org/
- Medical Subject Headings (MeSH): https://www.nlm.nih.gov/mesh/

## Notes

This dataset is included for reproducibility of the computational part of the bachelor's thesis. Licensing and reuse conditions may depend on the original dataset publication and the underlying PubChem data.
