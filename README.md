# Indian CPI Inflation Analysis (2013–2023)

An Excel-based data analytics project exploring India's Consumer Price Index (CPI), food-category price movements, year-over-year (YoY) inflation, the COVID-19 period, and the relationship between month-over-month movements in oils and fats and fuel and light.

## Project Overview

Inflation affects household purchasing power, business costs, pricing decisions, and economic policy. This project uses monthly All-India CPI index data to investigate how prices changed across categories and time.

**Tools:** Microsoft Excel, Power Query, PivotTables, charts, and Excel formulas  
**Project type:** Data cleaning, transformation, exploratory analysis, time-series analysis, and insight communication  
**Workbook:** `CPI_Inflation.xlsx`

> **Important distinction:** CPI is an index level; inflation is the percentage change in an index over time. The workbook calculates or compares percentage changes for selected analyses rather than treating the CPI index itself as an inflation rate.

## Business Questions

1. Which broad expenditure categories account for the largest share of the category-index totals used in the analysis?
2. How did average annual YoY CPI inflation change from 2017 to 2022?
3. Which food categories recorded the largest CPI increases and decreases over the selected 12-month comparison?
4. How did general and selected category indices/inflation measures behave around the COVID-19 period, including the first lockdown in 2020?
5. How closely did monthly percentage changes in **Oils and fats** and **Fuel and light** move together over the selected 2021–2023 period?

## Analysis and Key Findings

### 1. Broad-category contribution
- Food represents approximately **45.71%** of the total of the category-index values summed in the workbook's contribution analysis.
- “Other” represents approximately **15.09%**.
- Clothing and Footwear represents approximately **7.59%**.

**Interpretation:** Food is the largest category in this particular aggregation. This is a descriptive share of the summed index values used in the worksheet, **not an official CPI expenditure weight**. It should not be interpreted as the official contribution of food to headline inflation.

### 2. Average annual YoY inflation
The workbook's annual summary reports these average monthly YoY inflation values:

| Year | Average YoY inflation |
|---:|---:|
| 2017 | 3.25% |
| 2018 | 3.92% |
| 2019 | 3.82% |
| 2020 | 6.30% |
| 2021 | 5.60% |
| 2022 | 6.67% |

**Finding:** Among the years shown, 2022 has the highest average YoY inflation (approximately **6.67%**), followed by 2020 (approximately **6.30%**).

### 3. Food-category changes
For the selected 12-month endpoint comparison in the workbook:
- **Spices** increased from a CPI index of 187.1 to 218.0: a change of **30.9 index points**, or approximately **16.52%**.
- **Cereals and products** increased by 18.7 index points (approximately **12.06%**).
- **Oils and fats** decreased by 30.9 index points (approximately **15.38%**).
- **Vegetables** decreased by 21.3 index points (approximately **11.68%**).

These are changes in the category CPI index between the selected endpoints; they are not monthly inflation rates.

### 4. COVID-19 period analysis
The workbook prepares general and selected category data for a time-series comparison around the first COVID-19 lockdown period. It includes general index, food and beverages, health, housing, fuel and light, and transport and communication measures.

**Analytical focus:** Compare category movements before, during, and after March 2020, and distinguish changes in index levels from changes in YoY inflation. Interpret the pattern as a time-based association; this descriptive analysis alone does not establish that COVID-19 caused a particular change.

### 5. Oils and fats vs. fuel and light
The workbook calculates month-over-month percentage changes for Oils and fats and Fuel and light and uses Excel's `CORREL` function to assess their linear association over the selected period.

**Interpretation note:** Correlation measures how two series move together; it does not establish causation. The correlation value should be read from the `Q5_Correlation_Coeff` worksheet after opening the workbook in Excel and allowing formulas to calculate.

## Workflow

1. **Inspect the source data** and identify the sector, year, month, CPI item, CPI index, and broader category fields.
2. **Transform data with Power Query** to filter relevant sectors/categories, reshape data for selected questions, and prepare previous-period comparisons.
3. **Calculate inflation measures** using year-over-year and month-over-month index comparisons.
4. **Summarize results** with category summaries, annual averages, PivotTables, and charts.
5. **Interpret the results** in terms of household price pressures, category-level differences, and the limits of descriptive analysis.

## Workbook Guide

The Excel workbook contains the source data and question-specific analysis sheets, including:

- `Q1_Broader_Category_Filter`
- `Q1Broader_Category_Contribution`
- `Q2_CPI_Original`
- `Q2_CPI_Previous_Year`
- `Q2_Avg_YoY_Inflation% by Year`
- `Q3_Food_Inflation`
- `Q3_Food_Previous_Month`
- `Q3_Food_Category_Summary (Final`
- `Q4_COVID_PreviousYear`
- `Q4_COVID_final`
- `Q4_COVID_final_Chart`
- `Q4_COVID_final_Chart_data`
- `Q5_Correlation_Coeff`

The workbook also includes the source-data sheet and intermediate/helper sheets used during transformation.

## How to Use

1. Download or clone this repository.
2. Open `CPI_Inflation.xlsx` in Microsoft Excel.
3. Review the analysis worksheets listed above.
4. If formulas or charts do not immediately update, enable calculation and refresh applicable queries/PivotTables in Excel.
5. Use the README's findings as a guide, then verify the calculations and assumptions in the workbook.

## Limitations and Assumptions

- The analysis is based on the data and date ranges present in the supplied workbook, which extends through April 2023.
- Some worksheets are intermediate/helper outputs created during analysis; not every sheet is intended as a final presentation.
- The broad-category contribution is calculated from summed index values in the workbook and is **not** an official CPI basket weight or official inflation contribution.
- The food-category comparison uses selected start and end index values; its percentage change is not the same as a monthly or year-over-year inflation rate unless the endpoints represent that exact comparison.
- Correlation does not imply causation.
- The underlying data's original publisher, definitions, and usage terms should be credited according to the source from which the data was obtained.

## Skills Demonstrated

- Excel data analysis
- Power Query data transformation
- Data cleaning and reshaping
- CPI index and inflation calculations
- Year-over-year and month-over-month comparisons
- PivotTables and charts
- Correlation analysis
- Business interpretation and analytical caveats

## Repository Structure

```text
CPI-Inflation-Analysis/
├── CPI_Inflation.xlsx
├── README.md
└── .gitignore
```

## Author

**Pankhuri S.**  
Data Analytics Portfolio Project

For portfolio use, consider adding a screenshot of the most polished chart or summary view to the repository and linking it here once exported from Excel.
