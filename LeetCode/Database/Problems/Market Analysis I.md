⚙[문제보기](https://leetcode.com/problems/market-analysis-i/)



🔎문제 풀이
MySQL
```MySQL
SELECT user_id AS 'buyer_id', join_date, COUNT(order_id) AS 'orders_in_2019'
FROM Orders O RIGHT JOIN Users U 
ON O.buyer_id = U.user_id AND order_date LIKE '2019%'
GROUP BY 1;
```

MySQL
```MySQL
SELECT user_id AS 'buyer_id', join_date, COUNT(order_id) AS 'orders_in_2019'
FROM Orders O RIGHT JOIN Users U 
ON O.buyer_id = U.user_id AND YEAR(order_date) = '2019'
GROUP BY 1;
```


