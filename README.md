# Canada CPI Analysis with K-Means Clustering

## Overview
This project analyzes Canada's Consumer Price Index (CPI) data using K-Means clustering to identify distinct inflation regimes. It's part of the PROG8431 course's Problem Analysis Workshop 3.

**Author:** Jatinder Pal Singh (Student ID: 9083762)

## Dataset
The analysis uses Statistics Canada's Table 18‑10‑0005‑01 (Annual average CPI, 2021=100), which is provided as a tab‑separated file.

## Features
- Data cleaning and standardization
- Feature engineering including:
  - Year-over-Year percentage change
  - 3-year rolling volatility
- K-Means clustering implementation
- Visualization of:
  - CPI trends over time
  - Feature space analysis
- Silhouette score analysis for optimal cluster selection

## Technical Implementation
The project is implemented in Python using a Jupyter Notebook and includes:

### Key Dependencies
- pandas: Data manipulation and analysis
- numpy: Numerical computations
- matplotlib: Data visualization
- scikit-learn: Machine learning tools (KMeans, MinMaxScaler)

### Main Components
1. `CanadaCPIWideFormat` class with methods for:
   - Loading and transforming data
   - Feature engineering
   - Clustering analysis
   - Visualization
   - Results interpretation

### Clustering Approach
- Tests multiple k values (2 to 6 clusters)
- Uses silhouette scoring for optimal cluster selection
- Implements K-Means with standardized features

## Key Findings
- Optimal number of clusters: 4 (silhouette score = 0.453)
- Identified distinct inflation regimes in Canada's economic history
- Results useful for:
  - Forecasting
  - Economic policy analysis
  - Understanding historical CPI patterns

## Technical Notes
- Random seed set to 42 for reproducibility
- Data standardization using MinMaxScaler
- Implements robust error handling for data loading
- Supports both wide and long format data transformations

## Project Structure
```
Workshop3/
├── data/
│   └── CPI_annual_average_1810000501-eng_clean.csv
├── ClusteringKMeans_Workshop_3.ipynb
└── README.md
```

## Usage
1. Ensure all dependencies are installed
2. Load the Jupyter Notebook
3. Update the CSV_PATH if needed
4. Run all cells to perform the analysis

## Additional Information
For detailed information about the clustering methodology, including:
- Best value selection for k
- Algorithm convergence criteria
- Handling of multi-dimensional data

Refer to the detailed explanations in the notebook's markdown cells.