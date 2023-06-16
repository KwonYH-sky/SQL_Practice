⚙[문제보기](https://leetcode.com/problems/managers-with-at-least-5-direct-reports/)



🔎문제 풀이
MySQL
```MySQL
SELECT b.name
FROM Employee a JOIN Employee b ON a.managerId = b.id
GROUP BY b.id
HAVING COUNT(*) >= 5;
```