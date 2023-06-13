⚙[문제보기](https://leetcode.com/problems/customers-who-bought-all-products/)



🔎문제 풀이
MySQL
```MySQL
SELECT customer_id
FROM Customer
GROUP BY customer_id
HAVING COUNT(DISTINCT product_key) = (SELECT COUNT(*) FROM Product);
```
어려웠음