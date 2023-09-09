---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.15.1
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

```python
import tabula
import pandas as pd

```

```python
pdf_file_path = r"C:\Users\nithi\Downloads\Rosters\roster01.pdf"
excel_file_path = r"C:\Users\nithi\Downloads\Rosters\roster01.xlsx"
```

```python
tables = tabula.read_pdf(r"C:\Users\nithi\Downloads\Rosters\roster01.pdf", pages='all', multiple_tables=True)
```

```python
if tables:
    df = tables[0]
else:
    print("No tables found in the PDF.")
```

```python
if 'df' in locals():
    df.to_excel(r"C:\Users\nithi\Downloads\Rosters\roster01.xlsx", index=False)
    print(f"Table extracted and saved to {excel_file_path}")
else:
    print("No data frame (table) available to save.")
```

```python

```
