⚙[문제보기](https://leetcode.com/problems/sales-analysis-iii/)



🔎문제 풀이
MySQL
```MySQL
SELECT p.product_id, product_name
FROM Product p JOIN Sales s 
ON p.product_id = s.product_id 
GROUP BY p.product_id
HAVING MIN(sale_date) >= '2019-01-01' AND MAX(sale_date) <= '2019-03-31'
```