# fMRI-Connectome-MDD 
This repository provides a  reproducible pipeline for functional connectivity (FC) and machine learning (ML) analysis of resting-state fMRI data.
We analyze the preprocessed fMRIPrep outputs from the OpenNeuro dataset [**ds002748**](https://openneuro.org/datasets/ds002748).
The entire workflow is structured as step-by-step notebooks that run directly on Google Colab—no manual data downloading required.
<br>
<br>
<br>
## 📝Pipeline Overview:
### Notebook 1: Data Download & Time Series Extraction
- Downloads preprocessed fMRI data and confounds (~5 min)
- Extracts regional time-series based on AAL116 atlas.


### Notebook 2: Brain Activity Visualization
- Visualizes extracted time series as brain animations


### Notebook 3: Functional Connectivity Calculation
- Computes multiple FC measures (e.g., Pearson correlation, partial correlation, etc.)
- Creates feature vectors from different FC methods for comparison


### Notebook 4: Feature Selection & Dimensionality Reduction
- Applies feature selection techniques to identify the most discriminative connections between patients and controls


### Notebook 5: Classification & Interpretation
