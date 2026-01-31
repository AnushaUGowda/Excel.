# ☕ Coffee Sales Analysis – Excel Project
## 📌 Project Overview

This project is an interactive Excel sales dashboard created to analyze coffee sales data by combining multiple data sources and deriving business insights. The dashboard helps understand overall performance, customer behavior, product trends, and regional contributions.

## 🎯 Objective

The main objective of this project is to:

Combine sales, customer, and product data into a single analytical dataset

Clean and standardize raw data for better readability

Create key performance indicators (KPIs)

Build an interactive dashboard for business analysis

## 🗂️ Data Description

The dataset contains the following key fields:

Order ID

Order Date

Customer ID

Product ID

Customer Name

Country

Coffee Type

Roast Type

Size

Quantity

Unit Price

Sales

Loyalty Card

Data was originally stored in three tables:

Orders

Customers

Products

These were merged into a final table using lookup functions.

## Lookup & Data Integration Techniques:

### XLOOKUP
    =XLOOKUP(C2,customers!$A$1:$A$1001,customers!$B$1:$B$1001,,0)

To fetch Customer Name from the Customers table into the Orders table
  
   C2 → Value to search (Customer ID from Orders table)
  
   customers!$A$1:$A$1001 → Lookup column (Customer ID)

   customers!$B$1:$B$1001 → Return column (Customer Name)

This formula searches for the Customer ID in the Customers table and returns the corresponding Customer Name.

Likewise i used **XLOOKUP** to fetch Email and Country.

    =IF(XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0)=0,"",XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0))

    =XLOOKUP(C2,customers!$A$1:$A$1001,customers!$G$1:$G$1001,,0)

---

### INDEX AND MATCH

In this project, **INDEX with MATCH** was used as an alternative to XLOOKUP to retrieve product details dynamically from the Products table.

    =INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!I$1,products!$A$1:$G$1,0))

This formula returns a value from the Products table based on:

* Matching the Product ID

* Matching the column header

Breakdown:

1. MATCH for Row Number
   
   MATCH(orders!$D2, products!$A$1:$A$49, 0)
  
   Finds the row where Product ID in Orders matches Product ID in Products.

3. MATCH for Column Number
   
   MATCH(orders!I$1, products!$A$1:$G$1, 0)
   
   Finds the column position based on header name
   
   (e.g., "Unit Price", "Coffee Type", "Roast Type").

5. INDEX Function
   
   INDEX(products!$A$1:$G$49, row_num, col_num)
   
Returns the value from the exact row and column.

### 🧹 Data Transformation Using IFS (Standardization)

In this project, the IFS function was used to convert short product codes into meaningful full names for better readability and analysis.

    =IFS(I2="Rob","Robusta",I2="Exc","Excelsa",I2="Ara","Arabica",I2="Lib","Liberica")
This formula checks the value in cell I2 and returns the corresponding full coffee type name:

  If I2 = "Rob" → returns Robusta

  If I2 = "Exc" → returns Excelsa

  If I2 = "Ara" → returns Arabica

  If I2 = "Lib" → returns Liberica

## 🛠️ Tools & Techniques Used

Tool:Microsoft Excel

Techniques:XLOOKUP and INDEX-MATCH for table joins

Data cleaning and standardization (e.g., short codes to full names)

Calculated columns for Sales

Pivot Tables for analysis

Pivot Charts for visualization

Slicers for interactive filtering

## 📊 Key KPIs

Total Sales - Total revenue generated from all orders.

Total Orders - Total number of orders.

## 📈 Dashboard Features

The dashboard provides insights on:

Total Sales Over Time – Trend analysis using line chart

Top 5 Customers – Highest revenue customers

Sales Contribution by Country – Regional distribution

Total Sales by Coffee Type – Product performance

Slicers – Year, Month, Roast Type, Loyalty Card

All visuals are dynamically connected using slicers.

## 🔍 Key Insights

* A small group of customers contributes a significant portion of total revenue.
  
 they are,
<img width="297" height="146" alt="image" src="https://github.com/user-attachments/assets/2e02b004-d150-45ae-ae27-176f0da66e1b" />

* EXCELSA coffee type generate higher sales followed by liberica , then arabica then the least is robusta.
  
<img width="297" height="117" alt="image" src="https://github.com/user-attachments/assets/72d48078-5386-4671-84cd-6a2afd8fb358" />


* Sales peaked in 2021 year, indicating high revenue.
  
  <img width="194" height="91" alt="{A2F3CA8B-6456-43A8-B0DD-890E438325C5}" src="https://github.com/user-attachments/assets/1238e4f2-d22f-408d-a8fb-05ff364fb37c" />


* Customers without a loyalty card show stronger purchasing behavior than loyalty card holders.
  <img width="213" height="58" alt="image" src="https://github.com/user-attachments/assets/9a4bb43d-4a7f-4c2c-a521-ae0251b57779" />    

   <img width="240" height="62" alt="{4099F727-B48E-4DF3-88B1-0F128CE27065}" src="https://github.com/user-attachments/assets/7d641d87-5987-4568-9f65-e4cbda3116c3" />


