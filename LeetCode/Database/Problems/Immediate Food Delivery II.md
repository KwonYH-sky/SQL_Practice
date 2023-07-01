⚙[문제보기](https://leetcode.com/problems/immediate-food-delivery-ii/)



🔎문제 풀이
MySQL
```MySQL
SELECT ROUND(AVG(order_date = customer_pref_delivery_date) * 100, 2) AS immediate_percentage
FROM Delivery
WHERE (customer_id, order_date) IN (
  SELECT customer_id, MIN(order_date) FROM  Delivery GROUP BY customer_id
);
```

어려웠음