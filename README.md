<img width="714" height="130" alt="image" src="https://github.com/user-attachments/assets/90234afa-2b52-435b-98a1-aeb9c870a3ef" />

About: 
Instacart is a grocery delivery marketplace. Its revenue model depends on order frequency — the more often customers reorder, the more Instacart earns per customer over time. 

Problem Statement:
The growth team has noticed that a large share of customers who placed their first order never place a second one, and among those who do reorder, a meaningful portion go quiet after a few orders. At which step in the reorder journey are we losing the most customers, and which product categories show the highest drop-off? What behaviors in the first few orders separate high-value customers from at-risk ones — and how large is the gap between them?

Link to the dataset:
https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis/data 

About the data:
• orders.csv — One row per order. Contains user_id, order_number (1st, 2nd, 3rd order, etc.), order_dow (day of week), order_hour_of_day, and days_since_prior_order.
• order_products__prior.csv — One row per product per order, for all orders in a user’s history. Contains order_id, product_id, add_to_cart_order, and reordered (1 if the product was in a previous order).
• products.csv — Product names and their department and aisle IDs.
• departments.csv — Maps department_id to department name (e.g., produce, dairy eggs, beverages).






