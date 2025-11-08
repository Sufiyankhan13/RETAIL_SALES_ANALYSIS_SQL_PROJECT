# Retail Sales Analysis SQL Project

## Project Overview
This project demonstrates SQL skills through comprehensive analysis of retail sales data. The project covers data cleaning, exploration, and solving business problems using Microsoft SQL Server (MS SQL).

## Database Schema
The project uses a `RETAIL_SALES` table with the following structure:

| Column Name      | Data Type | Description                          |
|------------------|-----------|--------------------------------------|
| TRANSACTIONS_ID  | INT       | Unique transaction identifier        |
| SALE_DATE        | DATE      | Date of the transaction              |
| SALE_TIME        | TIME      | Time of the transaction              |
| CUSTOMER_ID      | INT       | Unique customer identifier           |
| GENDER           | VARCHAR   | Customer gender                      |
| AGE              | INT       | Customer age                         |
| CATEGORY         | VARCHAR   | Product category (Clothing/Beauty/Electronics) |
| QUANTIY          | INT       | Quantity of items sold               |
| PRICE_PER_UNIT   | DECIMAL   | Price per unit of product            |
| COGS             | DECIMAL   | Cost of goods sold                   |
| TOTAL_SALE       | DECIMAL   | Total sale amount                    |

## Project Structure
```
Retail-Sales-Analysis-SQL-Project--P1/
│
├── MSS-SQL.sql                          # Main SQL queries file
├── SQL - Retail Sales Analysis_utf.csv  # Dataset
└── Readme.md                            # Project documentation
```

## Key Features

### 1. Data Cleaning
- **Null Value Detection**: Identified records with missing values across all columns
- **Data Removal**: Deleted incomplete records to ensure data quality
- Ensured data integrity before analysis

### 2. Data Exploration
- Total sales count analysis
- Unique customer identification
- Product category distribution analysis

### 3. Business Problem Solutions

#### Q1: Sales on Specific Date
Retrieve all sales transactions made on a specific date (2022-11-05).

#### Q2: Category-Specific Analysis
Find all transactions for Clothing category with quantity > 3 in November 2022.

#### Q3: Sales by Category
Calculate total sales and order count for each product category.

#### Q4: Customer Demographics
Determine the average age of customers purchasing from the Beauty category.

#### Q5: High-Value Transactions
Identify all transactions with total sales exceeding $1000.

#### Q6: Gender-Based Category Analysis
Analyze transaction counts by gender across different product categories.

#### Q7: Best Selling Month
Calculate average sales per month and identify the best-performing month for each year using window functions (RANK).

#### Q8: Top Customers
Identify the top 5 customers based on total sales value.

#### Q9: Customer Distribution
Count unique customers per product category.

#### Q10: Sales by Time Shift
Categorize sales into shifts (Morning, Afternoon, Evening) and analyze order distribution:
- **Morning**: Before 12:00 PM
- **Afternoon**: 12:00 PM - 5:00 PM
- **Evening**: After 5:00 PM

## SQL Techniques Used

- **Basic Queries**: SELECT, WHERE, ORDER BY, GROUP BY
- **Aggregate Functions**: COUNT(), SUM(), AVG(), ROUND()
- **Date Functions**: FORMAT(), YEAR(), MONTH(), DATEPART()
- **Window Functions**: RANK() OVER (PARTITION BY)
- **Conditional Logic**: CASE statements
- **Data Manipulation**: DELETE
- **Subqueries**: Nested SELECT statements
- **Filtering**: DISTINCT, TOP N

## Getting Started

### Prerequisites
- Microsoft SQL Server (2016 or later)
- SQL Server Management Studio (SSMS) or Azure Data Studio

### Setup Instructions

1. **Clone or Download the Repository**
   ```bash
   git clone <repository-url>
   ```

2. **Import the Dataset**
   - Open SQL Server Management Studio
   - Create a new database (e.g., `RetailDB`)
   - Import the `SQL - Retail Sales Analysis_utf.csv` file into a table named `RETAIL_SALES`

3. **Run the SQL Queries**
   - Open `MSS-SQL.sql` in SSMS
   - Execute queries sequentially or select specific queries to run

## Key Insights

Based on the analysis, this project helps answer:
- Which product categories generate the most revenue?
- What are the peak sales periods (time of day, month, year)?
- Who are the most valuable customers?
- How do purchasing patterns differ by gender and age?
- What is the distribution of sales across different time shifts?

## Future Enhancements

- Add data visualization using Power BI or Tableau
- Implement stored procedures for repeated analyses
- Create views for commonly used queries
- Add more complex analytical queries (cohort analysis, customer lifetime value)
- Integrate with Python for advanced statistical analysis

## Author
This project was created as part of SQL learning and portfolio development.

## License
This project is open source and available for educational purposes.

---

**Note**: This project uses MS SQL Server syntax. Some queries may need modification for other SQL databases (MySQL, PostgreSQL, etc.).

