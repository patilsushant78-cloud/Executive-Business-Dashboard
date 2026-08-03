# Executive-Business-Dashboard
Executive Business Dashboard built in Power BI featuring KPI cards, revenue and profit analysis, regional and category insights, top-performing products, interactive filters, and drill-down capabilities. Designed using DAX, Power Query, and a star schema data model to support executive decision-making.

# Power BI Dashboard Project | Executive Business Dashboard

# Excited to share one of my latest **Power BI dashboard concepts**—an **Executive Business Dashboard** designed to provide leadership teams with a comprehensive view of business performance.

# Dashboard Highlights:
# Executive KPI Cards (Revenue, Profit, Margin, Growth, Orders & Customers)
# Revenue Trend Analysis
# Regional Sales Performance
# Category-wise Sales Breakdown
# Top 10 Products by Revenue
# Profit vs Sales Analysis
# Key Business Insights
# Interactive Slicers & Filters
# Clean, Executive-Friendly UI

# Skills Used:
# Power BI Desktop
# Power Query (M)
# DAX Measures
# Data Modeling (Star Schema)
# KPI Design
# Data Visualization
# Interactive Reporting

# The goal was to create a dashboard that enables executives to monitor business performance, identify trends, and make data-driven decisions through a single, interactive view.

# I'm continuously working on improving my dashboard design, performance optimization, and storytelling with data. Feedback and suggestions are always welcome!

# DAX Measures
Total Sales = SUM(Sales[Sales])

Total Profit = SUM(Sales[Profit])

Profit Margin =
DIVIDE([Total Profit],[Total Sales])

Orders =
DISTINCTCOUNT(Sales[Order ID])

Customers =
DISTINCTCOUNT(Sales[Customer ID])

Average Order Value =
DIVIDE([Total Sales],[Orders])

Sales LY =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(Calendar[Date])
)

Sales Growth % =
DIVIDE(
    [Total Sales]-[Sales LY],
    [Sales LY]
)

Target Achievement % =
DIVIDE([Total Sales],[Sales Target])

Average Profit =
AVERAGE(Sales[Profit])

Top Product Rank =
RANKX(
    ALL(Products[Product]),
    [Total Sales]
)

## Dashboard Preview

![Dashboard](dashboard.png)
