#data-wrangling

## Overview

This notebook demonstrates essential steps in the data wrangling process, including detecting and handling missing data, feature engineering, and data normalization.

### Detecting Missing Data
Two main methods I used to detect missing data:
1. `.isnull()`
2. `.notnull()`

These methods output a boolean value indicating whether the given value is missing. "True" means a value is missing, while "False" means the value is present.

#### Counting Missing Values
I counted the number of missing values in each column using a Python loop and the `.value_counts()` method.

### Handling Missing Data
There are two main ways to handle missing data:
1. Drop the missing data:
   - Drop entire rows
   - Drop entire columns (only when most data in the column is missing)
   
2. Replace the missing data:
   - Replace with the mean
   - Replace with the most frequent value
   - Replace using other techniques

In this dataset, none of the columns were sparse enough to drop entirely, so various replacement methods were applied.

### Data Transformation
- **Binning**: The data for `horsepower` is binned into three categories: 'Low', 'Medium', and 'High'.
- **Dummy Variables**: Dummy variables are created for categorical columns like `fuel-type` and `aspiration` to transform them into numerical features for analysis.
