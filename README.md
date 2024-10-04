# BREWERIES

## Project Title : Breweries Sales Analysis and Perfomance Dashboard

### Objective: 
The goal of this project is to design a comprehensive data analysis system for breweries database that tracks sales performance, profitability and regional distribution of products. This analysisn will help the company optimize its sales strategies and identify areas of growth.


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
