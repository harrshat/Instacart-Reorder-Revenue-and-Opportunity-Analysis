# 🛒 Instacart Reorder Revenue & Opportunity Analysis

<p align="center">
<img width="557" height="83" alt="image" src="https://github.com/user-attachments/assets/2087b505-c859-49ce-a33b-be77ae9a79f6" />
</p>

## 📌 About Instacart
Instacart is a grocery delivery marketplace whose unit economics depend heavily on repeat purchasing. Increasing reorder frequency directly increases customer lifetime value and marketplace revenue.

## 🎯 Problem Statement
Identify where customers drop off in the reorder journey and how high-value customers behave differently from at-risk customers.

**Key Questions:**
- At which order step does the largest customer drop-off occur?
- Which product categories show the weakest repeat purchasing?
- How do early ordering behaviors differ between high-value vs at-risk customers?
- How can Instacart identify at-risk users early and intervene?

## Link to the dataset:
https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis/data 

**Dataset constraint:** In this dataset, the number of unique users remains same from Orders 1–3, and customer drop-off is visible from Order 4 and boyond. This is a dataset limitation instead of real-world behavior where early churn after the first or second order is typically much higher. Hence, the analysis focuses on the earliest point where churn becomes observable in the data.

## 🗃️ Data Description
- orders.csv — One row per order. Contains user_id, order_number (1st, 2nd, 3rd order, etc.), order_dow (day of week), order_hour_of_day, and days_since_prior_order.
- order_products__prior.csv — One row per product per order, for all orders in a user’s history. Contains order_id, product_id, add_to_cart_order, and reordered (1 if the product was in a previous order).
- products.csv — Product names and their department and aisle IDs.
- departments.csv — Maps department_id to department name (e.g., produce, dairy eggs, beverages).

## Key Findings:
1 - **Biggest funnel leak:** The largest single-step customer drop-off occurs between Order 4 → 5 (11.6%), making this the most critical retention moment in the lifecycle.

<p align="center">
<img width="570" height="351" alt="image" src="https://github.com/user-attachments/assets/f8536185-dcae-440d-aeee-4ad1fc1d0639" />
</p>

2 - **Revenue gap - Customer Segments:** - 
High-Value vs At-Risk customers: Median basket size is identical (8 items per order). 
Key difference = order frequency
  - High-Value: every 7 days
  - At-Risk: every 19 days

**Interpretation:** Retention opportunity lies in order cadence, not basket size.

<p align="center">
<img width="601" height="271" alt="image" src="https://github.com/user-attachments/assets/857b880a-3046-4f70-ac60-4018d3225988" />
</p>

3- **Category Leakage -  At-Risk Customers:**
Weakest repeat category: Personal Care. Only 28.6% of at-risk customers who purchased Personal Care in Order 1 reordered from the category by Order 3 — the lowest repeat rate among high-volume departments. These are consumable products expected to drive repeat purchases. Low reorder rates means that Instacart is losing this revenue to its competitors.
<p align="center">
<img width="554" height="333" alt="image" src="https://github.com/user-attachments/assets/ce10098f-5629-4a42-9931-d859a5738504" />
</p>

## Business Recommendation: 
Flag customers whose days_since_prior_order exceeds the median (7 days for High-Value) after Order 1. This identifies at-risk customers at the earliest actionable moment. A personalised in-app prompt at Order 2 featuring the top-dropped department from their Order 1 basket. 

Priority departments: Personal Care (lowest absolute reorder rate, 28.6%) and Alcohol (largest gap vs High-Value, 15 percentage points).







