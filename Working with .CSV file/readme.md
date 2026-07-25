# 📄 Working with CSV Files using Pandas

This folder contains my practice notebooks and datasets for learning how to work with **CSV (Comma-Separated Values)** files using the **Pandas** library in Python.

## 📚 Topics Covered

- Reading CSV files
- Loading data from local files
- Loading data from URLs
- Reading TSV (Tab-Separated Values) files
- Understanding important `read_csv()` parameters
- Handling missing values
- Handling bad rows
- Reading large CSV files efficiently

---

## 📌 `read_csv()` Parameters Practiced

| Parameter | Description |
|-----------|-------------|
| `filepath_or_buffer` | Path or URL of the CSV file |
| `sep` | Specifies the delimiter (`,` `;` `\t`, etc.) |
| `header` | Defines which row contains column names |
| `names` | Assigns custom column names |
| `index_col` | Sets a column as the DataFrame index |
| `usecols` | Reads only selected columns |
| `skiprows` | Skips specified rows while reading |
| `nrows` | Reads only a specified number of rows |
| `encoding` | Specifies the file encoding (UTF-8, Latin-1, etc.) |
| `dtype` | Sets data types for columns |
| `parse_dates` | Converts columns into datetime format |
| `na_values` | Defines custom missing values |
| `on_bad_lines` | Handles malformed rows (`error`, `warn`, `skip`) |
| `low_memory` | Optimizes memory usage for large files |

---

## 🛠️ Technologies Used

- Python 3
- Pandas
- Google Colab
- Jupyter Notebook

---

## 📂 Files

```
Working with CSV/
│── Working_with_CSV.ipynb
│── students.csv
│── countries.csv
│── zomato.csv
│── README.md
```

---

## 🚀 Sample Code

```python
import pandas as pd

df = pd.read_csv("students.csv")
print(df.head())
```

### Reading a TSV File

```python
df = pd.read_csv("students.tsv", sep="\t")
```

### Reading a CSV from URL

```python
import pandas as pd

url = "https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv"

df = pd.read_csv(url)
```

### Reading a File with Custom Column Names

```python
df = pd.read_csv(
    "students.csv",
    header=None,
    names=["ID", "Name", "Age", "City"]
)
```

### Handling Bad Rows

```python
df = pd.read_csv(
    "zomato.csv",
    on_bad_lines="skip"
)
```

### Reading a File with Encoding

```python
df = pd.read_csv(
    "zomato.csv",
    encoding="latin-1"
)
```

---

## 📖 Learning Outcomes

After completing this practice, I learned how to:

- Import CSV and TSV files into Pandas
- Read datasets from local storage and URLs
- Work with different separators and encodings
- Customize column names
- Handle malformed rows and missing values
- Explore datasets efficiently using Pandas

---

## 📌 Author

**Priyanshu Singh**

Learning Data Analysis and Machine Learning with Python & Pandas.
