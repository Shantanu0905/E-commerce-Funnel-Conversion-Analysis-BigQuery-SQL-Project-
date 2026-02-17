# E-commerce-Funnel-Conversion-Analysis-BigQuery-SQL-Project-
Project Overview
This project analyzes user behavior across an e-commerce sales funnel using event-level data in BigQuery.

The objective was to:
Measure user drop-off at each funnel stage
Calculate stage-to-stage conversion rates
Analyze performance by traffic source
Measure time-to-conversion
Evaluate revenue efficiency metrics
The analysis uses event data from the last 30 days.

Dataset Description:

The dataset contains event-level user interaction data with the following fields:
event_id – Unique event identifier
user_id – Unique user identifier
event_type – User action (page_view, add_to_cart, checkout_start, payment_info, purchase)
event_date – Timestamp of the event
product_id – Product interacted with
amount – Revenue generated (only populated for purchase events)
traffic_source – Acquisition channel
Each row represents one user event.

Key Analyses Performed
1️⃣ Funnel Stage Analysis
Unique users at each stage
Stage-to-stage conversion rates
Overall funnel conversion rate

2️⃣ Traffic Source Performance
Visitors by acquisition channel
Conversion rate per channel
Cart-to-purchase efficiency

3️⃣ Time-to-Conversion Analysis
Built a user-level journey model using earliest event timestamps to calculate:
Average time: view → cart
Average time: cart → purchase
Total average journey time
Sequential validation was applied to ensure correct event order.

4️⃣ Revenue Analysis
Total Revenue
Total Orders
Total Buyers
Average Order Value (AOV)
Revenue per Buyer
Revenue per Visitor
Revenue was calculated using the amount field from purchase events.

SQL Techniques Used:
Conditional aggregation (CASE WHEN)
CTE-based query structuring
Timestamp conversion from string
TIMESTAMP_DIFF() for journey time analysis
SAFE_DIVIDE() to prevent division errors

What This Project Demonstrates:
Funnel analytics implementation in SQL
Behavioral event modeling
Conversion rate analysis
Revenue metric calculation
Channel performance evaluation
