# BREWERIES

## Project Title : Breweries Sales Analysis and Perfomance Dashboard

### Objective: 
The goal of this project is to design a comprehensive data analysis system for breweries database that tracks sales performance, profitability and regional distribution of products. This analysisn will help the company optimize its sales strategies and identify areas of growth.

### Scope
1 Sales perfomance analysis
 - Calculate total sales, total quuantity sold and total profit for different categories such as brands, sales rep and countries
 - Identify the top performing brands and sales rep
   
2 Profitability analysis
 - Determine profit margins for brands
   
3 Regional sales identity
 - Compare sales across different countries
   
4 Seasonal trends and growth analysis
 - Track sales performance over time to dentify seasonal peak and dips.


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

SELECT (PROFIT/COST)*100, BRANDS FROM Breweries_DB.`international breweries` ;
```
