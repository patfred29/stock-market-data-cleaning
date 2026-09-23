# Stock Market Dataset Cleaning & Analysis

Independent project — cleaned and analyzed a 1,000-row mock stock market dataset.

## What was wrong with the raw data
- Unstructured personal/user fields mixed with financial data (usernames, IPs, gender fields)
- Market cap values inconsistently formatted (some as "$1.12B", others as "N/A")
- Missing values scattered across multiple columns
- Some rows had no sector assigned at all

## What I did
- Cleaned and restructured the dataset into a proper table with clear headers (Username, Domain, First/Last Name, Market, Symbol, Sector, Industry, Market Cap, Price, Volume, etc.)
- Built a formula to flag data completeness per row:
  `=IF(OR(N:N="n/a", O:O="n/a", P:P="n/a"), "Missing", "Complete")`
  — checks multiple key columns at once and labels each row as Missing or Complete
- Built a Pivot Table summarizing total trading Volume by Sector across the full dataset, including an "N/A" category for unlabeled sectors and a "(blank)" category for missing sector entries — kept visible rather than hidden, to accurately reflect data quality

## Tools
Excel (IF/OR logic, structured Tables, Pivot Tables)

## Files
- `MOCK_DATA.xlsx` — original raw dataset
- `MOCK_DATA_Cleaned2.xlsx` — cleaned dataset with completeness-check formula and Pivot Table (sheets: MOCK_DATA, pivot_chart)
