# Syntecxhub_Time_Series_Categorical_Charts
**Project Overview**

This project was completed as part of Week 2 internship tasks under the guidance of Syntecxhub (@Syntecxhub).
The goal was to analyze sales data across multiple years and regions, clean and prepare the dataset, and communicate insights using appropriate visualizations.


**Repository Structure**

├── data/
│   ├── 2025sales.csv
│   ├── Salestill2024.csv
│   ├── customer_central.csv
│   ├── customer_east.csv
│   ├── customer_south.csv
│   └── customer_west.csv
│
├── charts/
│   ├── overall monthly_sales_trend.png
│   ├── yearly_sales_trend.png
│   ├── quarterly_sales_trend.png
|   ├── monthly_sales_trend.png
│   ├── sales_by_segment.png
│   ├── sales_by_region.png
│   ├── sales_by_ship_mode.png
│   ├── profit_share_region.png
│   └── profit_share_ship_mode.png
│
├── Sales_Summary.txt
├── sales_analysis.ipynb
└── README.md

**Step 1: Dataset Loading**

Multiple datasets was used:
Sales data (up to 2024 and for 2025)
Customer data split by region (Central, East, South, West)
All datasets were loaded using pandas.read_csv() and stored in DataFrames for processing.

**Step 2: Dataset Combination**

Customer datasets were combined into a single customer table using pd.concat()
Sales datasets were merged together
The sales and customer data were merged using Customer_ID as the common key
This resulted in one unified dataset containing sales, customer demographics, region, and shipping information.

**Step 3: Data Cleaning & Preparation**

Key cleaning steps included:
Handling missing values (identified using .isnull().sum())
Converting date columns (Order_Date, Ship_Date) to proper datetime format
Resolving mixed date formats (d-m-y and d/m/y)
Ensuring correct data types:
Age converted to integer
Barcode_Value treated as identifier (not numerical calculation)
Postal_Code treated as identifier
Extracting:
Order_Year
Order_Month
Order_Month_Name
Order_Quarter

**Final dataset contained 9,999 records and 20 columns, ready for analysis.**

**Step 4: Exploratory Data Analysis & Visualizations**

**Line Charts (Time Series Analysis)**

The following trends were analyzed: 
1. Overall Monthly Sales Trend: Shows long-term sales movement across all months. Helps identify growth and seasonal patterns
2. Yearly Sales Trend (2021–2025): Aggregated yearly view. Shows business growth over time
3. Quarterly Sales Trend: Highlights seasonal patterns and quarterly performance
4. Monthly Sales Trend for 2025 Only: Focuses on recent performance. Helps identify short-term fluctuations.
   
**Bar Charts (Category Comparison)**

6. Sales by Segment:Consumer segment recorded the highest sales
7. Sales by Region:Compares performance across regions
8. Sales by Shipping Mode: Evaluates which shipping methods drive more sales.
   
**Pie & Doughnut Charts (Proportional Analysis)**

10. Profit Share by Region (Pie Chart): Shows each region’s contribution to total profit
11. Profit Share by Shipping Mode (Doughnut Chart): Highlights profitability distribution across shipping methods.
All charts were saved as PNG files for documentation and portfolio use
 
**Step 5: Summary Insights Export**

A text summary was generated and saved as Sales_Summary.txt with the following insights:

    **Key Findings**
Total Sales: 2,298,577.23
Number of Months Analyzed: 49
Highest Sales Month: May 2025
Highest Sales Segment: Consumer
This summary was exported programmatically using Python file handling.

**Tools & Libraries Used**

Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook

**Learning Outcomes**

Through this project, I gained hands-on experience in:
Combining multiple datasets
Data cleaning and type handling
Time-series aggregation (monthly, quarterly, yearly)
Choosing appropriate visualizations
Communicating insights clearly through charts and summaries.

**Acknowledgement**

This project was completed as part of my internship training under the guidance of Syntecxhub.
Special thanks to @Syntecxhub for the structured tasks and mentorship.
