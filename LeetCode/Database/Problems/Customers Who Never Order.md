⚙[문제보기](https://leetcode.com/problems/customers-who-never-order/)



🔎문제 풀이
MySQL
```MySQL
SELECT name AS 'Customers'
FROM Customers C LEFT JOIN Orders O ON C.id = O.customerId
WHERE O.id IS NULL;
```
