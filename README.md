# fMRI-Connectome-MDD 
This repository provides a  reproducible pipeline for functional connectivity (FC) and machine learning (ML) analysis of resting-state fMRI data.
We analyze the preprocessed fMRIPrep outputs from the OpenNeuro dataset [**ds002748**](https://openneuro.org/datasets/ds002748).
The entire workflow is structured as step-by-step notebooks that run directly on Google Colab—no manual data downloading required.
<br>
<br>
<br>
## 📝Pipeline Overview:
### Notebook 1: Data Download & ROI Time-Series Extraction
- Downloads preprocessed resting-state fMRI data and confound regressors from OpenNeuro (~5 min).
- Applies confound regression, detrending, band-pass filtering, and z-score standardization.
- Extracts ROI time series using the AAL3 atlas.
- Saves the extracted time-series matrices and metadata as: <br>
  timeseries/ <br>
  ├── sub-01_timeseries.npy <br>
  ├── ... <br>
  ├── sub-72_timeseries.npy <br>
  └── extraction_metadata.json

### Notebook 2: Functional Connectivity Calculation
- Computes multiple FC measures (e.g., Pearson correlation, partial correlation, etc.)
- Creates feature vectors from different FC methods for comparison


### Notebook 3: Feature Selection & Dimensionality Reduction
- Applies feature selection techniques to identify the most discriminative connections between patients and controls


### Notebook 4: Classification & Interpretation
