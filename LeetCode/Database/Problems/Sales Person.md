⚙[문제보기](https://leetcode.com/problems/sales-person/)



🔎문제 풀이
MySQL
```MySQL
SELECT name
FROM SalesPerson
WHERE name NOT IN
        (SELECT S.name
        FROM Orders O RIGHT JOIN SalesPerson S ON O.sales_id = S.sales_id
        LEFT JOIN Company C ON O.com_id = C.com_id
        WHERE C.name = 'RED')
```
