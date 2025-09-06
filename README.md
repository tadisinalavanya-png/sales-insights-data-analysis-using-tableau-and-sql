<h1>Sales Insights - Data Analysis using Tableau and SQL</h1>

This project focuses on delivering Sales Insights for an India-based hardware company through comprehensive Data Analysis using Tableau and SQL.

For more details on the analytical framework, refer to the Data Analyst Roadmap.

### Project Overview

- Performed India-based hardware company sales insights - A Data Analysis project.
- Developed ETL mappings using SQL to extract data from unstructured sources and transformed it to a staging area to conduct data cleaning and design a star schema data model on Tableau.
- Developed a Tableau dashboard to perform analysis, producing quantitative visualizations in Tableau to draw valuable insights based on different parameters affecting company performance year-on-year and provide business solutions.

## Technologies Used

* Advanced Excel
* MySQL | SQL Server
* Tableau | Power BI
* Statistics

## Project Foundations and Certifications

- Data Visualization with Tableau - by Simplilearn
- Databases and SQL for Data Science with Python - by IBM
- Statistics for Data Science with Python - by IBM
- Data Visualization with Advanced Excel - by PWC

## Project - India based Hardware company Sales Insights - Data Analysis performed on Tableau and SQL
  
### Tableau Dashboard Link

### Problem Statements
The Sales Director requires visibility into the performance of the company across various Indian states to inform strategic discounting and promotional decisions.

- Q1. Revenue breakdown by cities.
- Q2. Revenue breakdown by years and months.
- Q3. Top 5 customers by revenue and sales quantity.
- Q4. Top 5 Products by revenue.
- Q5. Net Profit and Profit Margin by Market.

### Approach - Project Planning and Aims Grid
  
#### 1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that were previously unavailable to the sales team for decision support and automate reporting to reduce manual time spent in data gathering.

#### 2. Stakeholders: Who will be involved?
- Sales Director
- I.T. Team
- Customer Service Team
- Data and Analytics Team

#### 3. End Result: What do we want to achieve?
An automated dashboard providing quick and latest sales insights in order to support data-driven decision making.

#### 4. Success Criteria: What will be our success criteria?
- Dashboards uncovering sales order insights with the latest data available.
- Sales team able to take better decisions and prove 10% cost savings of total spend.
- Sales analysts stop data gathering manually in order to save 20% of their business time and reinvest it in value-added activity.

### Data Analysis - Approach
The project follows a structured pipeline: Data Discovery -> Data Cleaning/ETL -> Data Modeling -> Dashboard Building -> Insights Generation.

### Setup Process
  
Step 1: Download the database files (db_dump.sql or db_dump.xlsx).

Step 2: Import the data into MySQL and perform ETL (Extract, Transform, Load) processes as required.

Step 3: Utilize Tableau Public or Tableau Desktop to perform the Data Analysis.
  
Step 4: Connect Tableau to the MySQL database or Excel data source.
  
Step 5: Save the analysis file in .twb or .twbx format.

## Data Analysis Using SQL
  
1. Show all customer records
    SELECT * FROM customers;

2. Show total number of customers
    SELECT count(*) FROM customers;

3. Show transactions for Chennai market (market code for Chennai is Mark001)
    SELECT * FROM transactions where market_code="Mark001";

4. Show distinct product codes that were sold in Chennai.
    SELECT distinct product_code FROM transactions where market_code="Mark001";

5. Show transactions where currency is US dollars.
    SELECT * from transactions where currency="USD";

6. Show transactions in 2020 joined by date table.
    SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7. Show total revenue in year 2020.
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR" or transactions.currency="USD";
	
8. Show total revenue in year 2020, January Month.
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR" or transactions.currency="USD");

9. Show total revenue in year 2020 in Chennai.
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

## Data Analysis Using Tableau 
  
### Tableau Dashboards: Revenue and Profit Analysis

#### Creating Star Schema in Tableau
The data model is designed using a Star Schema, connecting the central transactions fact table with dimension tables including customers, date, markets, and products to ensure efficient querying and visualization.

#### Tableau Dashboard - Revenue Analysis
The Revenue Analysis dashboard provides a high-level view of total revenue, sales quantity, and revenue trends over time, segmented by geography and customer base.

#### Tableau Dashboard - Profit Analysis
The Profit Analysis dashboard focuses on bottom-line metrics, including profit margin percentages and net profit contributions by market and product category.
  
## Project References

1. Tableau Project Dashboard: Sales Insights - Data Analysis using Tableau
2. MySQL Installation and Configuration
3. OLTP and OLAP Architectural Differences
4. Star Schema Design: Fact Tables and Dimension Tables
  
## Related Data Projects

- Spotify Data Analysis using Python
- Statistics for Data Science using Python
- Python Lessons for Data Analysis
- Python Libraries for Data Science

## Maintainer

### Lavanya Tadisina
**Business Analyst**

Business Analyst with over 4 years of experience delivering data-driven solutions and process optimization across financial services and enterprise IT environments. Proficient in SQL, Tableau, and Power BI, with a focus on translating complex data into actionable business insights.

- Email: tadisinalavanya@gmail.com
- GitHub: github.com/ltadisina
- LinkedIn: linkedin.com/in/lavanyatadisina