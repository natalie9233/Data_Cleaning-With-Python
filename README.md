# Customer Call List Cleaning with Python & pandas

This project turns a sample Excel contact list into a standardized CSV. It demonstrates duplicate removal, text cleanup, phone and address formatting, and filtering based on a do-not-contact flag.

## Results

| Step | Records |
| --- | ---: |
| Original Excel rows | 21 |
| Exact duplicates removed | 1 |
| Explicit do-not-contact records removed | 4 |
| Remaining records without a 10-digit phone removed | 3 |
| Remaining rows without a Do Not Contact flag removed | 3 |
| Cleaned CSV rows | 10 |

For example, a number written as `202/555/0142` becomes `202-555-0142`. Phone numbers stored as numbers in Excel are read as text before formatting. The export excludes records with a blank do-not-contact flag and retains records with incomplete addresses. Entirely blank columns are omitted.

## Notebook and data

- [Original project notebook](customer_call_list_cleaning.ipynb) contains the original cleaning steps. To rerun it, install `pandas` and `openpyxl` and place the sample Excel file beside the notebook.
- [Sample Excel file](data/Customer%20Call%20List.xlsx) contains the fictional input records.
- [Cleaned CSV](data/Customer%20Call%20List%20Cleaned.csv) contains the 10 records from the follow-up export. That export also excluded rows with a blank Do Not Contact flag.

## Tutorial credit

This practice project follows [Data Cleaning in Pandas | Python Pandas Tutorials](https://www.youtube.com/watch?v=bDhvCp3_lYw) by Alex The Analyst.
