# Pandas 

Pandas is a Python library used to analyze and work with data.

## Key Concepts

- **Series**: A Series is like a column of a table.
- **DataFrame**: A DataFrame is the whole table.

## Accessing Data

To get a specified row:
```python
df.loc[n]  # By index
df.loc["day2"]  # By label
```

## Loading Data

You can load CSV files into a Pandas DataFrame with the following code:
```python
import pandas as pd
df = pd.read_csv("example.csv")
```