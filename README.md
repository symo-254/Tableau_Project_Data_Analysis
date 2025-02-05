# Tableau_Project_Data_Analysis
## Dashboard File
[View the Final Dashboard](https://public.tableau.com/app/profile/simon.macharia)  
My final dashboard file [Sales Performance in the United States.twbx](https://github.com/symo-254/Tableau_Project_Data_Analysis/blob/main/Sales%20Performance%20in%20the%20United%20States.twbx)
# Sales DashBoard
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
### 1. KPI Overview & Sales Trends
– Display a summary of total sales, profits and quantity for the current year and the previous year.  
– Present the data for each KPI on a monthly basis for both the current year and the previous year.  
– Identify months with highest and lowest sales and make them easy to recognize.  

![KPI](https://github.com/user-attachments/assets/ad1faefc-4895-448d-bd9f-7e083311e58a)

- Used calculated feilds to calculate total sales, profits and quantity for current| previous year and also the max and min sales  

``IF YEAR([Order Date])=[Select Year] THEN [Sales] END``      
``IF YEAR([Order Date])=[Select Year]THEN [Profit]END ``   
``IF YEAR([Order Date])=[Select Year]THEN [Quantity]END``    
``IF SUM([Current Y Sales])=WINDOW_MAX(SUM([Current Y Sales]))THEN SUM([Current Y Sales])``  
``ELSEIF SUM([Current Y Sales])=WINDOW_MIN(SUM([Current Y Sales]))THEN SUM([Current Y Sales]) END``  

- Used bans to display the total sales for the current year and percentage difference between current and orevious year sales  
- Used line chart to visualize and compare the  monthly total sales, profits and Quantity for current year and previous year.  
- Used circles to display the highest and lowest sales for the current year.  

### 2. Product Subcategory Comparison
 – Compare sales performance by different product subcategories for the current year and the previous year.   
 – Include a comparison of sales with profit.  
 
 ![Sales $ Profits By Subcategory](https://github.com/user-attachments/assets/94646efe-a1ce-4675-9b1f-6d1d7c4984ff)  

- Bar Charts: To display the sales performance for each subcategory.
- Color Coding: To differentiate between the current year and the previous year.
- Dual-Axis Chart: To compare sales and profit within the same visualization.
- Tooltips: To provide additional information on hover, such as exact sales and profit figures.
 
### 3. Weekly Trends for Sales & Profit
 – Present weekly sales and profit data for the current year.  
 – Display the average weekly values.  
 – Highlight weeks that are above and below the average to draw attention to sales & profit performance.  

 ![Sales $ Profits Trends over time](https://github.com/user-attachments/assets/c23dd919-09f2-4282-800d-ba92058ec322)  

- Line Charts: To display the weekly trends for both sales and profit.  
- Calculated Fields: To compute the average weekly sales and profit.  
- Color Coding: To highlight weeks that are above and below the average.  
- Reference Lines: To mark the average weekly values on the chart for easy comparison.  
- Annotations: To emphasize significant weeks with notable sales and profit performance.

# Customer DashBoard  
![Customer Dashboard](https://github.com/user-attachments/assets/2cd695ef-1b17-47c5-baeb-08c0bf1e9dbd) 

## Introduction  
The customer dashboard aims to provide an overview of customer data, trends and behaviors. It will help marketing teams and management to understand customer segments and improve customer satisfaction.  

## Customer Dashboard Requirements  
### 1. Customer Trends
 – Present the data for each KPI on a monthly basis for both the current year and the previous year. 
 – Identify months with highest and lowest sales and make them easy to recognize.   

![Screenshot 2025-02-05 083214](https://github.com/user-attachments/assets/a343152a-bbe0-4d26-b206-1379d2973325)

- Bans: To Display total monthly customers, sales per customer, total orders and percentage difference between current and previuos year.  
- Line Charts: To display the monthly trends for each KPI.  
- Color Coding: To highlight the highest and lowest sales months.  
- Annotations and Tooltips: To provide additional context and information on significant data points.  
- Calculated Fields: To determine the monthly values for each KPI and identify the extreme values.  
  ``Current year customers-- IF YEAR([Order Date]) =[Select Year] THEN [Customer ID (Customer.csv)] END ``  
  ``Previous Year customers-- (COUNT([CY Customers])-COUNT([PY Customers]))/COUNT([PY Customers])``  
  ``Sales per customer-- SUM([Current Y Sales])/COUNTD([CY Customers])  SUM([Previous Y Sales])/COUNTD([PY Customers])``  
  ``([CY Sales per Cust]-[PY Sales per Cust])/[PY Sales per Cust]``  
  ``Max|Min Customer count-- IF COUNTD([CY Customers])= WINDOW_MAX(COUNTD([CY Customers]))
THEN COUNTD([CY Customers])
ELSEIF COUNTD([CY Customers])= WINDOW_MIN(COUNTD([CY Customers]))
THEN COUNTD([CY Customers])
END``    
### 2. Customer Distribution by Number of Orders 
Represent the distribution of customers based on the number of orders they have placed to provide insights into customer behavior, loyalty and engagement.  

![Customer distribution](https://github.com/user-attachments/assets/278fa729-cc76-4b1c-96aa-848513014093)  
- Histograms: To visualize the frequency distribution of customers based on the number of orders.
- Annotations: To highlight significant customer segments with the highest and lowest number of orders.  

### 3. Top 10 Customers By Profit
 – Present the top 10 customers who have generated the highest profits for the company.  
 – Show additional information like rank, number of orders, current sales, current profit and the last order date.  

![Top 10 Customers by profits](https://github.com/user-attachments/assets/ece6cc36-60ca-4fda-a2ab-4d299ac7cc18)  
- Tables: To provide a detailed breakdown of additional information for each customer.  
- Calculated Fields: To compute the required metrics such as total profit, total sales, and number of orders.  
- Filters: To ensure only the top 10 customers are displayed in the visualization.  




 
