
The final output is an interactive dashboard that helps business users make **data-driven decisions**.

---

## Key KPIs Tracked

### Average Revenue per Day
**What it shows:**  
The average amount of revenue generated per day.

**Why it matters:**  
Helps management understand daily business health and track growth or decline over time.

---

### Total Orders
**What it shows:**  
Total number of orders placed during the selected time period.

**Why it matters:**  
Indicates overall demand and customer activity.

---

### Items Available
**What it shows:**  
Total number of unique menu items.

**Why it matters:**  
Helps understand menu size and variety compared to performance.

---

## Key Insights & Takeaways

### Least & Most Ordered Items

**What was analyzed:**
- Item name
- Category
- Number of times each item was ordered

**Key Takeaways:**
- Certain items (like burgers and popular Asian dishes) dominate order volume.
- Some items receive very few orders and may need improvement or removal.
- Demand is concentrated on a small set of high-performing items.

**Business Action:**
- Ensure top-selling items are always available.
- Review low-performing items for pricing, taste, or menu placement.

---

### Highest Spend Orders

**What was analyzed:**
- Order ID
- Items purchased
- Total spend per order

**Key Takeaways:**
- High-spend orders usually contain multiple premium items.
- Italian dishes frequently appear in high-value orders.
- Some customers consistently place large orders.

**Business Action:**
- Create combo meals or bundles using premium items.
- Promote upselling during peak hours.

---

### Order Volume by Time

**What was analyzed:**
- Order hour
- Number of orders per hour

**Key Takeaways:**
- Peak order times are:
  - Lunch hours (12 PM – 1 PM)
  - Evening hours (5 PM – 7 PM)
- Order volume drops significantly after 9 PM.

**Business Action:**
- Schedule more staff during peak hours.
- Run discounts or offers during slow hours to boost demand.

---

### Order Volume by Date

**What was analyzed:**
- Orders per day over time

**Key Takeaways:**
- Order volume is stable with normal daily fluctuations.
- No extreme spikes or drops, indicating consistent business performance.

**Business Action:**
- Suitable for long-term planning and forecasting.
- Seasonal trends can be added later for deeper analysis.

---

### Cuisines to Focus On

**What was analyzed:**
- Total orders per category
- Total revenue per category
- Average price per category

**Key Takeaways:**
- Asian cuisine generates the highest overall revenue.
- Italian and Mexican cuisines also perform strongly.
- American cuisine has high order volume but relatively lower revenue.

**Business Action:**
- Expand Asian cuisine offerings.
- Introduce premium items in popular cuisines.
- Review pricing strategy for high-volume but low-revenue categories.

---

## Why This Dashboard Works Well

- Metrics are **pre-calculated in the ETL layer**, avoiding incorrect aggregations.
- Each chart answers a **specific business question**.
- Clean separation between:
  - Item-level analysis
  - Order-level analysis
  - Time-based trends
  - Category-level strategy
- Easy for non-technical users to understand.

---

## Tools & Technologies Used

- **Database:** MySQL
- **ETL:** Python (Pandas)
- **Automation:** Email + Google Apps Script
- **Data Storage:** Google Sheets
- **Visualization:** Looker Studio

---

## Final Outcome

This project delivers:
- Clear visibility into restaurant performance
- Actionable insights for menu optimization
- A scalable foundation for future analytics

---

## Author

**Pranab Debnath**  
Data & Analytics Enthusiast  
GitHub: https://github.com/alsopranab
