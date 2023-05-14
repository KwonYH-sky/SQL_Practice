⚙[문제보기](https://leetcode.com/problems/recyclable-and-low-fat-products/description/)


🔎문제 풀이
MySQL
```MySQL
SELECT product_id FROM Products
WHERE low_fats = "Y" AND recyclable = "Y"
```
