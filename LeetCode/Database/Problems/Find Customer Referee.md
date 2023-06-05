⚙[문제보기](https://leetcode.com/problems/find-customer-referee/)



🔎문제 풀이
MySQL
```MySQL
SELECT name
FROM Customer
WHERE COALESCE(referee_id, 0) != 2;
```
