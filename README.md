
# Financial Sample — Power BI Dashboard

## 📊 Project Overview

This project analyzes the Financial Sample dataset using Microsoft Power BI to explore sales performance, profit, product performance, and business trends.

The dashboard provides an interactive overview of financial performance across different countries, segments, and time periods. It helps users identify key trends and compare sales and profitability to support data-driven decisions.

## 🎯 Project Objectives

- Analyze total sales and total profit.
- Track sales performance over time.
- Compare sales and profit across Months.
- Identify the best-performing products.
- Analyze performance across business segments.
- Compare actual sales with previous-year sales.
- Create an interactive dashboard using Power BI.

## 📁 Dataset

**Dataset:** Financial Sample

The dataset contains financial and sales information for different products, countries, segments, and time periods.

### Main Columns

| Column | Description |
|---|---|
| Segment | Customer or business segment |
| Country | Country where sales occurred |
| Product | Product sold |
| Discount Band | Discount category |
| Units Sold | Number of units sold |
| Manufacturing Price | Cost to manufacture one unit |
| Sale Price | Selling price per unit |
| Gross Sales | Sales before discounts |
| Discounts | Total discount amount |
| Sales | Sales revenue after discounts |
| COGS | Cost of Goods Sold |
| Profit | Profit generated |
| Date | Transaction date |
| Month Name | Name of the month |
| Year | Year of the transaction |

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop** — Dashboard creation and data visualization.
- **Power Query** — Data cleaning and transformation.
- **DAX** — Calculated measures and time intelligence.
- **Data Modeling** — Relationships and date table management.

## 🧹 Data Preparation

The following preparation steps were performed in Power BI:

- Inspected the dataset and column data types.
- Checked the date column and configured it for time-based analysis.
- Reviewed missing values and data consistency.
- Verified numerical columns used in calculations.
- Created measures using DAX.
- Prepared fields for charts, tables, and KPI cards.

## 📐 DAX Measures

The following measures can be used in the dashboard.

### Total Sales

```dax
Total Sales =
SUM(Sheet1[Sales])
```

### Total Profit

```dax
Total Profit =
SUM(Sheet1[Profit])
```

### Total Units Sold

```dax
Total Units Sold =
SUM(Sheet1[Units Sold])
```

### Profit Margin

```dax
Profit Margin =
DIVIDE([Total Profit], [Total Sales], 0)
```

Format this measure as a percentage.

### Sales Previous Year

```dax
Sales Previous Year =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Calendar'[Date])
)
```

This measure requires a properly configured Calendar table related to `Sheet1[Date]`.

### Sales Growth %

```dax
Sales Growth % =
DIVIDE(
    [Total Sales] - [Sales Previous Year],
    [Sales Previous Year],
    0
)
```

Format this measure as a percentage.

## 📈 Dashboard Visualizations

The dashboard can include the following visuals:

| Visualization | Purpose |
|---|---|
| KPI Cards | Display total sales, total profit, units sold, and profit margin |
| Line Chart | Analyze sales trends over time |
| Bar Chart | Compare sales by product |
| Map | Explore sales performance by country |
| Donut Chart | Show the distribution of sales by segment |
| Slicers | Filter the dashboard by year, country, segment, and product |

## 🔍 Business Questions

This project aims to answer the following questions:

1. What are the total sales and total profit?
2. Which product generates the highest sales?
3. Which product generates the highest profit?
4. Which country has the highest sales?
5. Which business segment contributes the most revenue?
6. How do sales and profit change over time?
7. How do current sales compare with the previous year?
8. Which countries and products should receive more attention?

## 💡 Key Insights

After completing the analysis, summarize your actual findings here.

- **Sales Performance:** 2014 recorded the highest sales.
- **Product Performance:** Paseo generated the highest sales.
- **Geographical Performance:** The United States had the highest sales.
- **Segment Analysis:** The Government segment contributed the most to total sales.
- **Time Trends:** Sales fluctuated throughout the year, with higher sales in some months.
- **Year-over-Year Growth:** Sales increased compared with the previous year.


## 🖼️ Dashboard Preview

![Financial Sample Power BI Dashboard](images/images/financial-dashboard.PNG)

## 📂 Project Structure

```text
financial-sample-power-bi/
│
├── images/
│   └── financial-dashboard.png
│
├── Financial_Sample_Dashboard.pbix
└── README.md
```

## 🚀 How to Use

1. Download or clone this repository.
2. Open `Financial_Sample_Dashboard.pbix` using Power BI Desktop.
3. Explore the report pages and visualizations.
4. Use the slicers to filter results by country, segment or date.
5. Review the KPI cards and charts to understand business performance.

## 📚 What I Learned

Through this project, I practiced:

- Preparing and transforming data with Power Query.
- Creating DAX measures for financial analysis.
- Working with date tables and time intelligence.
- Comparing sales and profitability across categories.
- Building interactive dashboards with slicers.
- Translating business questions into meaningful visualizations.
- Communicating analytical findings through a dashboard.


**Data Analytics Portfolio Project**

Tools: Power BI | Power Query | DAX
