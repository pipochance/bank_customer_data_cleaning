# Credit Banking Project

This project is a data analysis exercise using Python and Excel, focused on monthly customer spending and repayment behaviors. The aim is to compute dues, apply interest, and calculate monthly profit for a fictional banking system using real-world data handling techniques.

## Dataset Information

- **File name:** `Credit_Banking_Project.xlsx`
- **Sheets used:**
  - `Spend` – contains customer spending records.
  - `Repayment` – contains customer repayments.

##  Objectives

1. **Merge customer spend and repayment data.**
2. **Group data by month and customer.**
3. **Calculate monthly due amounts.**
4. **Apply an interest rate of 2.9% on due amounts.**
5. **Calculate monthly bank profit from interest.**
6. **Output results into a new Excel sheet `Monthly_Report`.**

---

## Key Steps Performed

### Data Preprocessing
- Read the Excel file using `pandas`.
- Converted the `Month` columns in both sheets to `datetime`.
- Extracted `Year-Month` as a new `Month` column using `.dt.to_period("M")`.

### Data Aggregation
- Grouped spend and repayment data by `Customer` and `Month`.
- Merged both grouped datasets.

### Interest & Due Calculations
- Computed the due amount for each customer each month.
- Applied 2.9% interest only on **positive dues** (where the customer didn’t repay in full).

### Monthly Profit Calculation
- Summed all interest values per month to get the bank's monthly profit.

---

## Output
A new sheet named `Monthly_Report` is created in the same Excel file (`Credit_Banking_Project.xlsx`), which includes:
- Monthly spend
- Monthly repayment
- Due amount
- Interest charged
- Profit per month (bank's earnings)

---

## Tools Used
- Python (Jupyter Notebook)
- Pandas
- Excel (`xlsxwriter`)
- Matplotlib / Seaborn *(optional for visualizations)*

---

## How to Run

1. Clone the repository or download the files.
2. Make sure you have the required packages installed:
   ```bash
   pip install pandas openpyxl xlsxwriter
3. Open the .ipynb file in Jupyter Notebook and run all cells.
4. Check the Excel output in the same directory.

Contact
Created by Priyanshu Tiwari
Feel free to reach out for questions/suggestions
