⚙[문제보기](https://leetcode.com/problems/bank-account-summary-ii)


🔎문제 풀이
MySQL
```MySQL
SELECT name, SUM(amount) AS 'balance'
FROM Users U JOIN Transactions T ON U.account = T.account
GROUP BY T.account
HAVING balance > 10000;
```
