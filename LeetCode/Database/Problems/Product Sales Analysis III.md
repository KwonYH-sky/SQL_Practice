⚙[문제보기](https://leetcode.com/problems/product-sales-analysis-iii)



🔎문제 풀이
MySQL
```MySQL
SELECT product_id, year as first_year, quantity, price
FROM Sales
WHERE (product_id, year) IN (
  SELECT product_id, MIN(year) FROM Sales
  GROUP BY product_id
)
```