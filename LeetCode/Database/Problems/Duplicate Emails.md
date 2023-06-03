⚙[문제보기](https://leetcode.com/problems/duplicate-emails/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT email AS 'Email'
FROM Person
GROUP BY email
HAVING COUNT(*) >= 2;
```
