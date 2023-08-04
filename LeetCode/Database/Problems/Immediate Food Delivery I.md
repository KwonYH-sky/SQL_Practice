⚙[문제보기](https://school.programmers.co.kr/learn/courses/30/lessons/164670)



🔎문제 풀이
MySQL
```MySQL
SELECT ROUND(SUM(order_date = customer_pref_delivery_date) / count(*) * 100, 2) AS 'immediate_percentage'
FROM Delivery;
```