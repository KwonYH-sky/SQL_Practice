⚙[문제보기](https://leetcode.com/problems/product-sales-analysis/)



🔎문제 풀이
MySQL
```MySQL
SELECT product_name, year, price
FROM Sales S JOIN Product P ON S.product_id = P.product_id;
```
