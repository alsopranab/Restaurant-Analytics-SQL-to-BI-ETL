#  Restaurant Analytics — SQL to BI ETL Pipeline

<p align="center">
  <img src="dashboard/restaurant_analytics_dashboard.png" width="900">
</p>

<p align="center">
  <i>Fig 1. Final Looker Studio Visualization</i>
</p>

---

##  Architecture Workflow

<p align="center">
  <img src="workflow/workflow.jpg" width="900">
</p>

<p align="center">
  <i>
    Fig 2. ETL Workflow Diagram
  </i>
</p>

---

## Live Dashboard (Looker Studio)
```
https://lookerstudio.google.com/reporting/256749c2-2924-493d-a924-ab75e8233c9a
```


---

## Problem Statement

Restaurants generate large volumes of transactional data every day, but this data often remains locked inside databases and is not easily usable for decision-making.

The business needed:
- Visibility into **most and least ordered items**
- Identification of **high-value orders**
- Insights into **peak and low ordering hours**
- Understanding of **top-performing cuisines**
- A fully **automated reporting workflow**

This project solves these problems using a **simple, automated, end-to-end ETL pipeline**.

---

## Project Overview

This is a **demo ETL and analytics project** that moves data directly from **SQL to business intelligence**.

The pipeline:
- Extracts raw data from MySQL
- Transforms it into analytics-ready metrics using Python
- Automatically delivers data to Google Sheets and Looker Studio

The result is **zero manual reporting** and **always up-to-date KPIs**.

---

## Tech Stack

- **Database:** MySQL  
- **ETL & Transformation:** Python (pandas)  
- **Automation:** Gmail (SMTP) + Google Apps Script  
- **Visualization:** Looker Studio  

---

## Data Source

The project uses the following tables:

- `order_details`
- `menu_items`

These tables are joined to create a **single analytics-ready dataset**.

---

## ETL Process

### Extract
- Pulls data from MySQL using SQL queries
- Uses Python MySQL connector and cursor execution

### Transform
- Cleans and standardizes data types
- Removes duplicates and handles null values
- Adds time-based features (order hour)
- Calculates item-level, order-level, and category-level metrics

### Load
- Generates a final consolidated CSV file
- Sends the CSV automatically via email
- Loads data into Google Sheets
- Feeds Looker Studio for visualization

---

## Business Questions Answered

- Which items are **most and least ordered**
- Which orders generate the **highest revenue**
- When do **peak and slow hours** occur
- Which cuisines perform best and should be **expanded**

---

## Output

- **Final Dataset:** `restaurant_analytics_final.csv`
- **Used for:**
  - Google Sheets (data layer)
  - Looker Studio dashboard
  - Automated email reporting

---

## Automation

- KPI reports are sent automatically via email
- Designed for future scheduling using **cron jobs**
- Pipeline can be extended for daily or hourly refreshes

---

## Author

**Pranab Debnath**  
GitHub: https://github.com/alsopranab
