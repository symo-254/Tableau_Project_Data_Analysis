# Tableau Sales DashBoard
![Sales Dashboard](https://github.com/user-attachments/assets/6536bd31-91bb-4349-8985-c22f34ebc195)

## Introduction  
The purpose of sales dashboard is to present an overview of the sales metrics and trends in order to analyze year-over-year sales performance and understand sales trends. 

## Tableau Skills Used  
 - Charts
 - Calculated Fields
 - Parameter
 - Tableau Functions
 - Dashboard

## Sales Dashboard Requirements  
### KPI Overview & Sales Trends
– Display a summary of total sales, profits and quantity for the current year and the previous year.  
– Present the data for each KPI on a monthly basis for both the current year and the previous year.  
– Identify months with highest and lowest sales and make them easy to recognize.  

![KPI](https://github.com/user-attachments/assets/ad1faefc-4895-448d-bd9f-7e083311e58a)

Used calculated feilds to calculate total sales, profits and quantity for current| previous year and also the max and min sales  
```IF YEAR([Order Date])=[Select Year] THEN [Sales] END```    
``IF YEAR([Order Date])=[Select Year]THEN [Profit]END ``   
``IF YEAR([Order Date])=[Select Year]THEN [Quantity]END``    
``IF SUM([Current Y Sales])=WINDOW_MAX(SUM([Current Y Sales]))THEN SUM([Current Y Sales])ELSEIF SUM([Current Y Sales])=WINDOW_MIN(SUM([Current Y Sales]))THEN
  SUM([Current Y Sales])
  END``  
Used bans to display the total sales for the current year and percentage difference between current and orevious year sales  
Used line chart to visualize and compare the  monthly total sales, profits and Quantity for current year and previous year.  
Used circles to display the highest and lowest sales for the current year.  

### Product Subcategory Comparison
 – Compare sales performance by different product subcategories for the current year and the previous year.   
 – Include a comparison of sales with profit.  
 
 ![Sales $ Profits By Subcategory](https://github.com/user-attachments/assets/94646efe-a1ce-4675-9b1f-6d1d7c4984ff)  
 


### Weekly Trends for Sales & Profit
 – Present weekly sales and profit data for the current year.

 – Display the average weekly values.

 – Highlight weeks that are above and below the average to draw attention to sales & profit performance.
