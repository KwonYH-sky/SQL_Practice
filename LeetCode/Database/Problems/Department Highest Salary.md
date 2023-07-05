⚙[문제보기](https://leetcode.com/problems/department-highest-salary/)



🔎문제 풀이
MySQL
```MySQL
SELECT Department, Employee, Salary
FROM (
  SELECT d.name AS Department, e.name AS Employee, e.salary AS Salary, DENSE_RANK() OVER(PARTITION BY e.departmentId ORDER BY e.salary DESC) AS rk
  FROM Employee e JOIN Department d ON e.departmentId = d.id
) TB
WHERE rk = 1;
```