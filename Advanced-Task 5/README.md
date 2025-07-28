# Task 5: Interactive Business Dashboard in Streamlit

## Objective:
Develop an interactive dashboard using Streamlit for analyzing sales, profit, and segment-wise performance from the Global Superstore dataset.

## Dataset:
- **Name:** Global Superstore Dataset
- **Content:** Sales transactions with fields like Region, Category, Sub-Category, Sales, Profit, Customer Name, and others.

## Data Preparation:
- Loaded and cleaned the dataset (`Global_Superstore2.csv`).
- Checked for missing values and handled data types.
- Extracted relevant features for KPIs (Sales, Profit, Region, Category, Sub-Category).
- Ensured categorical consistency and filtered usable columns.

## Dashboard Features:
Built using **Streamlit**, the app includes:

### Filters:
- Region
- Category
- Sub-Category

### KPIs and Visuals:
- **Total Sales**: Sum of all sales within selected filters.
- **Total Profit**: Aggregate profit for selected criteria.
- **Top 5 Customers**: Based on sales values.
- **Sales and Profit Charts**: Bar plots, Pie charts, etc., visualizing filtered data.
