# Wine Dataset Exploratory Data Analysis

A beginner-friendly data science portfolio project exploring chemical measurements from three wine cultivars.

## Objective
Explore the dataset, check data quality, analyze distributions and potential outliers, inspect correlations, and compare features across wine classes.

## Dataset
- Source: UCI Machine Learning Repository — Wine Recognition dataset
- Included file: `wine_data.csv`
- 178 observations
- 13 numerical predictor features
- 3 target classes (`target` and readable `class_name`)

The included CSV is generated from the built-in `scikit-learn` `load_wine()` dataset. The project does not require a dataset download when run from this folder.

## Tools
- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project structure
```text
wine_eda_project/
├── wine_data.csv
├── wine_eda.ipynb
├── requirements.txt
└── README.md
```

## Setup
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook
```

Open `wine_eda.ipynb` and run all cells from top to bottom.

## Analysis performed
1. Dataset loading and structure
2. Data types and summary statistics
3. Missing-value and duplicate checks
4. Class distribution
5. Feature histograms
6. IQR-based outlier screening
7. Correlation heatmap and strongest pairs
8. Class-wise summaries and boxplots
9. Pairwise relationships

## Important interpretation notes
- An IQR-flagged observation is not automatically an error.
- Correlation does not imply causation.
- This notebook is exploratory and does not claim predictive performance.
- Write the final findings in your own words after running and inspecting the outputs.

## Suggested GitHub description
Exploratory data analysis of the UCI Wine Recognition dataset using Python, pandas, NumPy, Matplotlib and Seaborn. Includes data quality checks, feature distributions, IQR outlier screening, correlation analysis and class-wise comparisons.

## Dataset reference
UCI Machine Learning Repository, Wine recognition dataset:
https://archive.ics.uci.edu/dataset/109/wine
