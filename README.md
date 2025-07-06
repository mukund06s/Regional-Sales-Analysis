# USA Regional Sales Analysis Dashboard

## Project Overview

This project provides a comprehensive analysis of Acme Co.'s 2014-2018 USA sales data through an interactive Power BI dashboard. The analysis focuses on identifying key revenue and profit drivers across products, channels, and regions while uncovering seasonal trends and outliers to optimize business strategies.

## Problem Statement

Analyze Acme Co.'s sales performance across different dimensions to:
- Identify top-performing products, channels, and regions
- Uncover seasonal patterns and anomalies
- Detect pricing and margin risks
- Inform strategic decisions for pricing, promotions, and market expansion

## Solution Overview

The Power BI dashboard delivers actionable insights through:
- Revenue and profit analysis by product, channel, and region
- Trend analysis with monthly/yearly sales patterns
- Outlier detection for pricing and margin risks
- Budget vs. actual performance comparisons
- Geographic visualization of sales performance

## Dataset

The analysis uses multiple interconnected datasets:
- **Sales Orders**: Transaction-level sales data (64,104 records)
- **Customers**: Client information (175 records)
- **Products**: Product catalog (30 items)
- **Regions**: Geographic data (994 locations)
- **State Regions**: US regional classifications
- **2017 Budgets**: Product budget targets

## Data Cleaning & Feature Engineering

Key transformations performed:
- Merged 6 source tables into a unified dataset
- Standardized column names and formats
- Calculated derived metrics:
  - Profit margin (Revenue - Cost)
  - Regional classifications (Northeast, Midwest, South, West)
  - Time-based features (year, month, quarter)
- Handled missing values and data type conversions

## Key Metrics & DAX Functions

| KPI | Description | DAX Example |
|------|------------|-------------|
| Total Revenue | Sum of all sales | `SUM('Sales'[revenue])` |
| Total Profit | Revenue minus costs | `SUM('Sales'[revenue]) - SUM('Sales'[cost])` |
| Profit Margin | Profit as % of revenue | `DIVIDE([Total Profit], [Total Revenue])` |
| Budget Variance | Actual vs budget comparison | `[Total Revenue] - [Budget Amount]` |
| YoY Growth | Year-over-year change | `DIVIDE([Current Year Revenue], [Prior Year Revenue]) - 1` |

## Visualizations
![image](https://github.com/user-attachments/assets/a55aab22-5186-40aa-adae-1889780829a2)

**1. Executive Summary**
- Key performance indicators
- Revenue/profit trends
- Budget achievement

**2. Product Analysis**
- Top/bottom performing products
- Revenue and margin by product
- Product mix analysis

**3. Channel Performance**
- Sales distribution by channel
- Channel profitability
- Channel growth trends

**4. Regional Analysis**
- Geographic sales heatmap
- Regional performance benchmarks
- Market penetration metrics

**5. Trend Analysis**
- Monthly/quarterly sales patterns
- Seasonal decomposition
- Year-over-year comparisons

## Project Structure

```
USA-Regional-Sales-Analysis/
├── Data/
│   ├── Regional Sales Summary.xlsx       # Raw data source
│   └── sales_cleaned.csv                # Processed dataset
├── Analysis/
│   └── EDA_Regional_Sales_Analysis.ipynb # Jupyter notebook with full analysis
├── Dashboard/
│   └── Regional_Sales_Dashboard.pbix    # Power BI dashboard
├── Reports/
│   ├── Sales_Analysis_Report.docx       # Detailed findings
│   └── Sales_Presentation.pptx          # Executive summary
└── README.md                           # Project documentation
```

## Requirements

- **Power BI Desktop** (latest version) to view/edit dashboard
- For Python analysis:
  - pandas
  - numpy
  - matplotlib/seaborn
  - jupyter

## How to Use

1. Clone the repository:
   ```
   git clone [repository-url]
   ```
2. Open `Regional_Sales_Dashboard.pbix` in Power BI Desktop
3. Explore the interactive visuals and filters
4. (Optional) Run the Jupyter notebook for additional analysis

## Future Enhancements

- Integrate real-time data connections
- Add predictive forecasting models
- Develop customer segmentation analysis
- Create automated report distribution

## Conclusion

This dashboard transforms Acme Co.'s sales data into strategic insights, enabling data-driven decisions for growth optimization and risk mitigation across products, channels, and regions.
