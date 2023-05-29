⚙[문제보기](https://leetcode.com/problems/list-the-products-ordered-in-a-period/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT product_name, SUM(unit) AS 'unit'
FROM Products P JOIN Orders O ON P.product_id = O.product_id
WHERE order_date LIKE '2020-02%'
GROUP BY P.product_id
HAVING unit >= 100;
```
