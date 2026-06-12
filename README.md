# fMRI-Connectivity-Analysis
A lightweight neuroimaging pipeline for:
- ROI extraction
- Functional connectivity analysis
- 
- 

## Analysis Pipeline
```text
Preprocessed fMRI
        │
        ▼
ROI Time Series Extraction
        │
        ▼
Functional Connectivity Matrix
        │
 ┌──────┴──────┐
 ▼             ▼
Edge Features  Graph Features
 │             │
 ├─ PCA        ├─ Degree
 └─            ├─ Clustering Coefficient
               ├─ Global Efficiency
               └─ Modularity
```
