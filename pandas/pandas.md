# Pandas 

Pandas is a Python library used to analyze and work with data.

## Key Concepts

- **Series**: A Series is like a column of a table.
- **DataFrame**: A DataFrame is the whole table.

### Accessing Data

To get a specified row:
```python
df.loc[n]  # By index
df.loc["day2"]  # By label
```

### Loading Data

You can load CSV (or JSON) files into a Pandas DataFrame with the following code:
```python
import pandas as pd
df = pd.read_csv("example.csv")
df = pd.read_json("example.json")
```

### Analyzing Data

You can look at the first rows of a DataFrame with the head() method:
```python
df.head()
```

You can look at the last rows of a DataFrame with the command tail() method:
```python
df.tail()
```

The DataFrames object has a method called info(), that gives you more information about the data set.
```python
df.info()
```