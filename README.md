# BREWERIES

## Project Title : Breweries Sales Analysis and Perfomance Dashboard

### Objective : 
The goal of this project is to design a comprehensive data analysis system for breweries database that tracks sales performance, profitability and regional distribution of products. This analysis will help the company optimize its sales strategies and identify areas of growth.

### Scope :
1 Sales perfomance analysis
 - Calculate total sales, total quuantity sold and total profit for different categories such as brands, sales rep and countries
 - Identify the top performing brands and sales rep
   
2 Profitability analysis
 - Determine profit margins for brands
   
3 Regional sales identity
 - Compare sales across different countries
   
4 Seasonal trends and growth analysis
 - Track sales performance over time to dentify seasonal peak and dips.

5 Visualization

### Tools Used :
- SQL - For data extraction, aggregation and performing complex analysis queries
- Excel - For advanced data visualization and dashboard creation

### Derived Metrics :
- Total sales
- Total profit
- Price per item
- Top 5 brand by profit
- Top 3 sales rep
  

### Data Analysis :
Codes Used
```SQL

SELECT BRANDS, SUM(COST), SUM(QUANTITY), SUM(PROFIT) 
  FROM Breweries_DB.`international breweries`
  GROUP BY BRANDS;
  
 SELECT  SALES_REP, SUM(COST), SUM(QUANTITY), SUM(PROFIT)
  FROM Breweries_DB.`international breweries`
  GROUP BY SALES_REP; 
  
   SELECT  COUNTRIES, SUM(COST), SUM(QUANTITY), SUM(PROFIT)
  FROM Breweries_DB.`international breweries`
  GROUP BY COUNTRIES; 
  
   SELECT  YEARS, SUM(COST), SUM(QUANTITY), SUM(PROFIT)
  FROM Breweries_DB.`international breweries`
  GROUP BY YEARS; 
  
  SELECT SUM(PROFIT) AS TOTAL_PROFIT, BRANDS 
  FROM Breweries_DB.`international breweries`GROUP BY BRANDS
ORDER BY TOTAL_PROFIT DESC 
LIMIT 5;

SELECT SUM(COST), SUM(PROFIT) AS TOTAL_PROFIT, SALES_REP
  FROM Breweries_DB.`international breweries`
  GROUP BY SALES_REP ORDER BY TOTAL_PROFIT
  LIMIT 3; 

SELECT DISTINCT BRANDS, (COST/QUANTITY) 
AS cost_per_item, (PROFIT/QUANTITY) AS profit_per_item 
FROM Breweries_DB.`international breweries`

SELECT DISTINCT BRANDS, (COST/QUANTITY) 
AS cost_per_item, (PROFIT/QUANTITY) AS profit_per_item 
FROM Breweries_DB.`international breweries`ORDER BY cost_per_item DESC LIMIT 2;
```
### Data Visualization :

![Breweries Linechart](https://github.com/user-attachments/assets/3b6a92e5-f4c9-4c5b-8f52-1523208dd883)


![Breweries piechart](https://github.com/user-attachments/assets/c50b351c-5fb0-4982-ba77-1ba548383495)


![Breweries barchart](https://github.com/user-attachments/assets/47128856-3cda-4a37-869e-e57a94ee8354)


