⚙[문제보기](https://leetcode.com/problems/customer-placing-the-largest-number-of-orders/)



🔎문제 풀이
MySQL
```MySQL
SELECT customer_number
FROM Orders
GROUP BY customer_number
ORDER BY COUNT(customer_number) DESC
LIMIT 1;
```
