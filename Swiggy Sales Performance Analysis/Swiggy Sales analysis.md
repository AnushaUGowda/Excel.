# 🍔 Swiggy Sales Data Analysis 

## 📌 Project Overview

This project focuses on analyzing **Swiggy food delivery data** and building an **interactive Excel dashboard** to extract meaningful business insights. The goal is to simulate a real-world **data analyst workflow** — from raw data cleaning to dashboard-driven decision-making.

The dashboard enables stakeholders to monitor **sales performance, customer behavior, food preferences, and regional trends** at a glance.

---

## 🛠️ Tools & Technologies

* **Microsoft Excel**

  * Power Query (ETL & data cleaning)
  * Pivot Tables & Pivot Charts
  * Slicers
  
* Excel formulas (DATE functions)

---

## 📂 Dataset Description

The dataset contains Swiggy order-level data including:

* Order Date
* Restaurant Name
* City & State
* Food Category
* Dish Type (Veg / Non-Veg)
* Order Value
* Customer Ratings

> The raw data was cleaned and transformed before analysis to ensure accuracy and consistency.

---

## 🧩 Data Understanding & Feature Engineering

In this project, the dataset was **already structured and analysis-ready**, so no aggressive data cleaning (such as duplicate removal or missing value treatment) was performed.

Instead, the focus was on **data understanding and feature engineering** aligned with the business problem.

Key steps performed:

* Reviewed column structure and data types
* Used the dataset as-is without assuming a primary key
* Created derived analytical columns:

  * Day Name (from Order Date)
  * Month and Quarter (for time-based analysis)
  * Veg / Non-Veg classification based on Dish Name keywords
* Directly built KPIs and pivot-based analysis from the dataset

This approach mirrors real-world scenarios where analysts often work with **read-only or business-provided datasets** and focus on extracting insights rather than modifying source data.

---

## 📊 Key Performance Indicators (KPIs)

| Metric              | Value   |
| ------------------- | ------- |
| Total Sales         | ₹53.01M |
| Total Orders        | 197.43K |
| Average Order Value | ₹268.51 |
| Average Rating      | 4.34    |
| Rating Count        | 5.59M   |

These KPIs provide a **high-level performance snapshot**.

---

## 📈 Analysis & Insights

### 🔹 Sales Trends

* **Monthly Trend**: Stable growth with peaks around May and August
* **Daily Trend**: Highest sales on Saturdays; weekends outperform weekdays
* **Weekly Trend**: Consistent order volume with minor fluctuations

### 🔹 Food Preference Analysis

* Veg food contributes the **majority of total sales**
* Non-Veg accounts for ~38% (₹20.3M), indicating strong but secondary demand

### 🔹 Regional Performance

* **Top Performing City**: Bengaluru (₹5.46M)
* Other key cities: Lucknow, Hyderabad, Mumbai, New Delhi
* Strong sales concentration in metro and Tier-1 cities

### 🔹 Quarterly Performance

| Quarter | Sales  | Avg Rating | Orders |
| ------- | ------ | ---------- | ------ |
| Q1      | ₹19.7M | 4.3        | 73.1K  |
| Q2      | ₹19.9M | 4.3        | 74.16K |
| Q3      | ₹13.4M | 4.3        | 50.17K |

Ratings remain consistent across quarters, indicating stable service quality.

---

## 🖼️ Dashboard Screenshot

Below is a snapshot of the interactive Excel dashboard created for this project:

> **Swiggy Sales Performance Dashboard **
> *(Includes KPIs, trends, city/state analysis, and Veg vs Non-Veg comparison)*

📷 **Screenshot:**
"Swiggy dashboard .png"



## 📌 Dashboard Features

* Interactive slicers (Month, Restaurant, Category)
* Dynamic KPI cards
* Trend charts (Daily, Weekly, Monthly)
* Geographic sales visualization by state
* Clean, management-friendly layout

The dashboard is designed for **quick decision-making**.

---

## 💡 Business Recommendations

* Focus marketing campaigns on **weekends**, especially Saturdays
* Strengthen partnerships in **high-performing cities** like Bengaluru
* Promote Veg categories more aggressively due to higher demand
* Use quarterly insights for seasonal offer planning

---

## 📌 Project Scope & Analytical Considerations

* The dataset was used as a **business reporting extract**, aligned with trend-level and aggregate analysis.
* The analysis focuses on **aggregated trends and KPIs**, where row-level uniqueness was not required.
* Customer-level behavior analysis was outside the scope due to the absence of unique customer identifiers.
* Veg / Non-Veg classification was derived using **business-rule-based keyword logic** to support high-level food preference analysis.
* Insights are interpreted within the scope and time range of the provided dataset.

---

## 🎯 Key Learnings

* End-to-end data analysis using Excel
* Translating business questions into KPIs
* Building interactive dashboards for stakeholders
* Applying real-world analytical thinking

