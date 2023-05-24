⚙[문제보기](https://leetcode.com/problems/problems/average-selling-price/)



🔎문제 풀이
MySQL
```MySQL
SELECT P.product_id, ROUND(SUM(price*units)/SUM(units), 2) as 'average_price'
FROM Prices P JOIN UnitsSold U 
ON P.product_id = U.product_id AND (purchase_date BETWEEN start_date AND end_date)
GROUP BY P.product_id;
```
