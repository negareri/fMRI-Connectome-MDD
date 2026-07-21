# fMRI-Connectome-MDD 
This repository provides a  reproducible pipeline for functional connectivity (FC) and machine learning (ML) analysis of resting-state fMRI data.
We use preprocessed fMRIPrep outputs from the OpenNeuro [**ds002748**](https://openneuro.org/datasets/ds002748) dataset.
The entire workflow is structured as step-by-step notebooks that run directly on Google Colab—no manual data downloading required.
<br>
<br>
<br>
## 📝Pipeline Overview:
### Notebook 1: Data Download & ROI Time-Series Extraction
- Downloads preprocessed resting-state fMRI data and confound regressors from OpenNeuro.
- Applies confound regression, detrending, band-pass filtering, and z-score standardization.
- Extracts ROI time series using the AAL3 atlas and exports the processed dataset for downstream analysis.

### Notebook 2: Functional Connectivity Calculation
- Computes static functional connectivity using Pearson correlation and partial correlation.
- Converts connectivity matrices into upper-triangular feature vectors and subject-by-feature matrices.
- Exports connectivity and feature representations for downstream machine learning.

### Notebook 3: Feature Selection & Dimensionality Reduction
- Explores feature selection and dimensionality reduction methods, including ANOVA, LASSO, and PCA.
- Visualizes and compares the selected features and reduced representations.
- Prepares feature reduction strategies for the machine learning pipeline.

### Notebook 4: Classification & Interpretation
