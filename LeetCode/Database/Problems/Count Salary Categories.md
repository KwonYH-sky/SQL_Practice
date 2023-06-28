⚙[문제보기](https://leetcode.com/problems/count-salary-categories/)



🔎문제 풀이
MySQL
```MySQL
SELECT "Low Salary" AS category, SUM(income < 20000) AS accounts_count
FROM Accounts
UNION
SELECT "Average Salary" AS category, SUM(income BETWEEN 20000 AND 50000) AS accounts_count
FROM Accounts
UNION
SELECT "High Salary" AS category,  SUM(income > 50000) AS accounts_count
FROM Accounts;
```