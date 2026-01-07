## Porblme Statement:

Restaurants generate large volumes of transactional data every day, but this data often remains locked inside databases and is not easily accessible for business decision-making.

The business needed:
- Visibility into **most and least ordered menu items**
- Understanding of **high-value orders and customer spending patterns**
- Identification of **peak and low ordering hours**
- Data-driven insights on **which cuisines to expand or optimize**
- An **automated reporting system** to eliminate manual data pulls

This project addresses these needs by building an **end-to-end ETL pipeline** that extracts data from MySQL, transforms it into analytics-ready format, and delivers KPI reports automatically.

---

## Project Overview

This project implements a complete **Extract → Transform → Load (ETL)** workflow using Python.

**Pipeline Flow:**
SQL > Python > Gmail > Sheet > BI Tool


---

## Tech Stack

- **Database:** MySQL
- **Language:** Python
- **Libraries:** pandas, mysql-connector-python, smtplib
- **BI Tool:** Looker Studio
- **Automation:** Cron (planned)

---

## Data Source

### Tables Used

- `order_details`
- `menu_items`

These tables are joined using the menu item identifier to create a single denormalized dataset for analysis.

---

## ETL Process

### 1. Extract
- Connects to MySQL using `mysql.connector`
- Fetches raw data using SQL queries
- Loads data into Pandas DataFrames

### 2. Transform
- Joins order and menu data
- Fixes data types (dates, time, price)
- Creates time-based features (order hour, day)
- Calculates:
  - Item order counts
  - Total spend per order
  - Category-level performance metrics

### 3. Load
- Produces a **single analytics-ready CSV**
- CSV is optimized for BI tools
- Automatically emailed to stakeholders

---

## Business Questions Answered

### 1. Least & Most Ordered Items
- Identifies which menu items sell the most and least
- Shows the category each item belongs to

### 2. Highest Spend Orders
- Finds high-value orders
- Shows how much was spent and on which items

### 3. Order Volume by Time
- Analyzes ordering trends by hour
- Highlights peak and slow business hours

### 4. Cuisine Performance
- Evaluates categories based on demand and revenue
- Helps decide which cuisines to expand or improve

---

## Output

- **File:** `restaurant_analytics_final.csv`
- **Contents:**
  - Clean dimensions (date, hour, item, category)
  - Pre-aggregated metrics for fast BI performance
- **Usage:**
  - Directly connected to Looker Studio
  - Sent via automated email

---

## Email Automation

- Sends KPI reports automatically using Gmail SMTP
- Attaches the final CSV file
- Uses environment variables for secure credentials

---
