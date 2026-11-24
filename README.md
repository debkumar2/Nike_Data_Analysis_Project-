
# Nike Sales Data Analysis

An end-to-end beginner-friendly data analysis project using Python to
clean, validate, and explore Nike sales data. The project focuses on
sales performance, product demand, revenue, and exploratory
profitability analysis.

## Project Overview

This project uses the **Nike Sales Uncleaned Dataset** from Kaggle. The
notebook starts with the raw dataset, standardizes and validates the
data, creates a calculated revenue field, and performs exploratory data
analysis (EDA).

The current notebook covers data preparation and **Phases 1--5**. It
does not yet include the later discount, time-based, or advanced
relationship-analysis phases.

## Dataset

-   **Dataset:** [Nike Sales Uncleaned
    Dataset](https://www.kaggle.com/datasets/nayakganesh007/nike-sales-uncleaned-dataset)
-   **Source file:** `Nike_Sales_Uncleaned.csv`
-   **Data type:** Retail sales transactions

The notebook works with fields including:

-   `Order_ID`
-   `Gender_Category`
-   `Product_Line`
-   `Product_Name`
-   `Sales_Channel`
-   `Region`
-   `Units_Sold`
-   `MRP`
-   `Discount_Applied`
-   `Revenue` (preserved as `Original_Revenue`)
-   `Profit`
-   `Order_Date`
-   `Size`

The exact available columns should be confirmed from the dataset version
being used.

## Tools & Technologies

-   Python
-   Jupyter Notebook / Kaggle Notebooks
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn

## Project Workflow

### Data Cleaning and Validation

The notebook includes the following preparation steps:

1.  Import the required Python libraries.
2.  Load the raw Nike sales dataset.
3.  Standardize column names.
4.  Inspect blank values and duplicate records.
5.  Standardize categorical text values.
6.  Standardize region names and product sizes.
7.  Convert relevant fields to numeric data types.
8.  Validate numeric values and missing values.
9.  Convert and validate order dates.
10. Preserve the original revenue field and calculate revenue for
    analysis.
11. Investigate unusual values in original revenue, units sold,
    discounts, MRP, and profit.
12. Review missing-value patterns and export the cleaned dataset.

**Calculated revenue formula**

``` python
Calculated_Revenue = Units_Sold * MRP * (1 - Discount_Applied)
```

The original revenue is retained as `Original_Revenue` so it can be
compared with the calculated value. This formula assumes
`Discount_Applied` is stored as a decimal fraction (for example, `0.20`
for 20%), as expected by the notebook calculation.

### Phase 1 -- Understanding the Dataset

-   Inspect the dataset structure and dimensions.
-   Review data types and column names.
-   Examine numerical and categorical fields.
-   Understand the dataset before analysis.

### Phase 2 -- Univariate Analysis

-   Analyze distributions of numerical columns.
-   Inspect numerical outliers using boxplots.
-   Identify categorical columns.
-   Review category frequencies.
-   Visualize categorical distributions.

### Phase 3 -- Sales Analysis

-   Calculate overall sales KPIs.
-   Analyze revenue by product line.
-   Identify the top 10 products by revenue.
-   Examine revenue contribution by gender category.
-   Analyze sales channels.
-   Compare regional sales performance.

### Phase 4 -- Profit Analysis

-   Calculate overall profit KPIs.
-   Classify profitable, loss-making, and zero-profit records.
-   Examine the profit distribution and potential outliers.
-   Compare profit by product line.
-   Identify and visualize the most profitable products.
-   Identify and visualize loss-making products.
-   Compare profitability by region and sales channel.
-   Calculate profit margin by product line.

**Profit-data caution:** The notebook treats the supplied `Profit` field
as an exploratory dataset value. It has not been independently
reconciled against a documented accounting formula. Negative profit
values are not automatically removed because they may represent losses.

### Phase 5 -- Product & Category Analysis

-   Compare units sold across product lines.
-   Identify the top 10 products by units sold.
-   Calculate average selling price by product line.
-   Compare product-line revenue across gender categories.
-   Build a product-level performance summary using units sold, revenue,
    and profit.

## Key Business Questions

The notebook is designed to help investigate questions such as:

1.  Which product line generates the highest revenue?
2.  Which products contribute the most revenue?
3.  Which sales channel and region generate the most sales?
4.  Which product lines and products generate the most profit?
5.  Which products are loss-making?
6.  Which region and sales channel contribute the most profit?
7.  Which product line has the highest profit margin?
8.  Which product line sells the highest number of units?
9.  Which products have the highest sales volume?
10. How does product-line revenue differ across gender categories?

Run the notebook to obtain the actual results and write evidence-based
observations. No numerical findings are stated here because results
depend on executing the notebook with the dataset.

## Repository Structure

A suggested GitHub repository structure:

``` text
Nike_Sales_Data_Analysis/
│
├── Nike_Sales_Data_Analysis.ipynb
├── README.md
├── data/
│   └── (cleaned dataset, if you choose to include it)
└── images/
    └── (optional charts and dashboard screenshots)
```

The raw Kaggle dataset is not included in this structure. Download it
from the dataset source and add it to your Kaggle environment or local
project folder.

## How to Run the Project

### Option 1: Kaggle

1.  Open the [Kaggle
    dataset](https://www.kaggle.com/datasets/nayakganesh007/nike-sales-uncleaned-dataset).
2.  Create a new Kaggle Notebook or upload the project notebook.
3.  Add the dataset to the notebook.
4.  Confirm that the CSV path in the data-loading cell matches the
    Kaggle input path.
5.  Run all cells from top to bottom.

### Option 2: Local Jupyter Notebook

1.  Clone or download this repository.
2.  Install the required libraries:

``` bash
pip install pandas numpy matplotlib seaborn jupyter
```

3.  Download `Nike_Sales_Uncleaned.csv` from Kaggle.
4.  Update the CSV path in the notebook's loading cell.
5.  Open Jupyter Notebook and run the notebook from top to bottom.

## Current Project Status

  -----------------------------------------------------------------------
  Component                           Status
  ----------------------------------- -----------------------------------
  Data cleaning and validation        Completed in notebook

  Phase 1 -- Understanding the        Completed in notebook
  Dataset                             

  Phase 2 -- Univariate Analysis      Completed in notebook

  Phase 3 -- Sales Analysis           Completed in notebook

  Phase 4 -- Profit Analysis          Completed through the included
                                      profitability sections

  Phase 5 -- Product & Category       Completed in notebook
  Analysis                            

  Phase 6 -- Discount Analysis        Not included yet

  Phase 7 -- Time-Based Analysis      Not included yet

  Phase 8 -- Correlation /            Not included yet
  Relationship Analysis               
  -----------------------------------------------------------------------

## Notes and Limitations

-   Run all notebook cells to generate the tables, charts, and actual
    findings.
-   Check the dataset's discount format before interpreting calculated
    revenue.
-   `Calculated_Revenue` is derived from units sold, MRP, and discount;
    it is not a replacement for validating the source's original
    revenue.
-   Profitability results are exploratory until the dataset's profit
    calculation is verified.
-   Do not interpret outliers or negative values as errors without
    investigation.
-   The notebook's input path may need to be changed when running
    outside Kaggle.

## Author

**DebKumar Mondal**

------------------------------------------------------------------------

If you find this project useful, feel free to explore the notebook,
reproduce the analysis, and suggest improvements.
"# Nike_Data_Analysis_Project-" 
