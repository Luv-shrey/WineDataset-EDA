# EDA Findings — Wine Recognition Dataset

These findings are calculated from the included `wine_data.csv`.

## Dataset and quality
- The file contains **178 rows** and **15 columns**: 13 numerical measurements, `target`, and the readable `class_name`.
- There are **0 missing values** and **0 exact duplicate rows**.
- Class counts are:
  - `class_0`: 59 observations
  - `class_1`: 71 observations
  - `class_2`: 48 observations
- The classes are not perfectly equal in size, but none is absent or extremely small in this dataset.

## Correlation observations
The strongest positive Pearson correlations include:
- `total_phenols` and `flavanoids`: **0.865**
- `flavanoids` and `od280/od315_of_diluted_wines`: **0.787**
- `total_phenols` and `od280/od315_of_diluted_wines`: **0.700**

One of the stronger negative correlations is:
- `malic_acid` and `hue`: **-0.561**

These are linear associations in this dataset; they do not establish causation.

## Selected class-wise averages

| Class | Alcohol | Flavanoids | Color intensity | Proline |
|---|---:|---:|---:|---:|
| class_0 | 13.74 | 2.98 | 5.53 | 1115.71 |
| class_1 | 12.28 | 2.08 | 3.09 | 519.51 |
| class_2 | 13.15 | 0.78 | 7.40 | 629.90 |

The class averages differ notably for the selected measurements. For example, `class_0` has the highest average proline and flavanoids among these three classes, while `class_2` has the highest average color intensity and the lowest average flavanoids.

## What not to conclude
- These averages do not prove that a feature alone identifies a class.
- Correlation does not imply causation.
- IQR outlier flags should be investigated, not automatically removed.
- This EDA does not evaluate a predictive model or establish performance on unseen data.

## Suggested conclusion for your notebook
The dataset contains 178 observations across three wine classes and has no missing values or exact duplicate rows. Class sizes are 59, 71 and 48. Several chemical measurements show substantial linear associations, particularly total phenols with flavanoids (r ≈ 0.865). Selected class-wise averages also differ: class_0 has higher mean proline and flavanoids, whereas class_2 has higher mean color intensity and lower mean flavanoids. These patterns suggest that the measured features vary across classes and merit further investigation. They are exploratory observations, not causal claims or evidence of model accuracy.
