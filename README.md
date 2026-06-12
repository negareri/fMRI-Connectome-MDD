# fMRI-Connectivity-Analysis
```text

A lightweight neuroimaging pipeline for: 
✓ ROI extraction 
✓ Functional connectivity analysis
✓
✓

## Analysis Pipeline

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
