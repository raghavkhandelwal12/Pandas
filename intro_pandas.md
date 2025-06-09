# What is Pandas?

- Pandas is a fast, Powerful, flexible, and easy-to-use `open-source Python library` for `data manipulation and data analysis`.
- It provides data structures like:

1. `Series` : One-dimensional labeled arrays.
2. `DataFrame` : Two-dimensional tables, similar to Excel or SQL tables.

# Pandas is well suited from different types of data.

1. `Pandas works with Heterogeneous data(works with different data) in sql database, and excel sheet`.
2. `Pandas works with ordered and unordered time series data(order not matter)`.
3. `Arbitary Matrix` data (homogeneously typed or heterogeneous) with row and column labels.

# Key Features:
- Handling of `Missing data`.
- Supports for `multiple file formats(CSV, Excel, Json, SQL etc)`. 
- `Powerful groupby` functionality for data aggregation.
- `Time series functionaliy`.
- Tools for reshaping, merging, and pivoting datasets.

  # Where Is Pandas Used?

- Pandas is used everywhere `structured data is involved`, including:

1. `Data Science` : Exploratory data analysis, feature engineering.

2. `Business` : Reports, Dashboards, sales analysis, KPIs.

3. `Finance` : Stock data analysis, backtesing, risk modeling.

4. `Healthcare` : Patient data analysis, health records, clinical trial data.

5. `E-Commerce` : Customer Behaviour, product sales, A/B Testing.

6. `Web APIs` : Reading, processing, and analyzing API response data.

7. `Academia` : Statistical Analysis, Experimental results.

**It is widely used in** : 

- `Python Notebooks(jupyter, Google Colab)`.
- `Kaggle Competitions`.
- `Machine Learning Workflows`.
- `Data pipelines in Production`.

  # Why Use Pandas?

1. `Convenient Data Structures` : DataFrame and Series are intutive and powerful for working with tabular data.

2. `Powerful Tools` : Perform aggregations, joins, reshaping, and sorting with ease.

3. `Robust File I/O` : Read and Write to multiple formats like CSV, Excel, JSON, SQL etc.

4. `Missing Data Handling` : Provides methods like `fillna(), dropna, interpolate`.

5. `Integration with Other Libraries` : Works well with NumPy, Matplotlib, seaborn PyArrow etc.

6. `Automatic and explicit data alignment` : Object can be explicitly aligned to a set of labels, or the user can simply ignore the labels let `Series, DataFrame` Automatic aligned the data for in computation.

7. `Size Mutability` : Row, Columns can be `inserted or deleted` in the dataframe and higher dimensional Objects.

8. Powerful, flexible `group by` functionality to perform split-apply-combine operations on data sets, for both aggregating and transforming data.

9. `Easy Handling of missing data(represented as NaN) in floating point as well as non-floating point data`.

# How to Install Pandas for windows.
- To install the pandas for the windows run the this command

```
pip install pandas
```
or
```
python -m pip install pandas
```


# To check the Pandas is working or not 

```
import pandas as pd
print(pd.__version__)
```
