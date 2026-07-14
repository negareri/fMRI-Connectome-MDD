# fMRI-Connectome-MDD 
This repository provides a  reproducible pipeline for functional connectivity (FC) and machine learning (ML) analysis of resting-state fMRI data.
We use preprocessed fMRIPrep outputs from the OpenNeuro [**ds002748**](https://openneuro.org/datasets/ds002748) dataset.
The entire workflow is structured as step-by-step notebooks that run directly on Google Colab—no manual data downloading required.
<br>
<br>
<br>
## 📝Pipeline Overview:
### Notebook 1: Data Download & ROI Time-Series Extraction
- Downloads preprocessed resting-state fMRI data and confound regressors from OpenNeuro (~5 min).
- Applies confound regression, detrending, band-pass filtering, and z-score standardization.
- Extracts ROI time series using the AAL3 atlas.
- Saves the extracted time-series matrices and metadata as AAL3_timeseries_all_subjects.zip: <br>
  timeseries/ <br>
  ├── sub-01_timeseries.npy <br>
  ├── ... <br>
  ├── sub-72_timeseries.npy <br>
  └── extraction_metadata.json

### Notebook 2: Functional Connectivity Calculation
- Computes static functional connectivity using Pearson correlation and partial correlation.
- Converts connectivity matrices into upper-triangular feature vectors for machine learning.
- Generates four outputs:
  - Pearson FC matrices
  - Partial FC matrices
  - Pearson feature vectors
  - Partial feature vectors

### Notebook 3: Feature Selection & Dimensionality Reduction
- Applies feature selection techniques to identify the most discriminative connections between patients and controls


### Notebook 4: Classification & Interpretation
