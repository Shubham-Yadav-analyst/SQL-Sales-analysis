# SQL Sales Analysis - MySQL

Complete sales data analysis using advanced SQL queries.

## Tools Used
- MySQL Workbench
- Joins, CTEs, Window Functions, Group By, Subqueries

## Files Included
- `Sales_Analysis_SQL.txt` - All SQL queries
- `CTE + JION _ SQL.jpg` - CTE & Join query screenshot
- `Window_function_SQL.jpg` - Window function result

## Key Business Questions Solved
1. Total Sales by Region & Product
2. Top 3 Salespersons - Using RANK()
3. Monthly Sales Trend
4. Category-wise Performance using CTE + JOIN

## Sample Query
```sql
-- Top Performing Region
SELECT region, SUM(sales_amount) as total_sales
FROM sales
GROUP BY region
ORDER BY total_sales DESC;

-- Window Function Example
SELECT salesperson, region, sales_amount,
RANK() OVER (PARTITION BY region ORDER BY sales_amount DESC) as rank_in_region
FROM sales;
