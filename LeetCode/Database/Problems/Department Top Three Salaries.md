⚙[문제보기](https://leetcode.com/problems/department-top-three-salaries/)



🔎문제 풀이
MySQL
```MySQL
SELECT D.name AS Department, E1.name AS Employee, E1.salary AS Salary
FROM Employee E1 JOIN Department D ON E1.departmentId = D.id
WHERE 3 > (
  SELECT COUNT(DISTINCT E2.salary) # 0이 나오면 가장 큰 액수 1이면 2번째, 2면 3번째..
  FROM Employee E2
  WHERE E2.salary > E1.salary
  AND E1.departmentId = E2.departmentId 
);
```

or

MySQL
```MySQL
SELECT Department,Employee,Salary
FROM
(SELECT
d.name AS Department,
e.name AS Employee,
e.Salary AS Salary,
dense_rank() over(PARTITION BY e.departmentId ORDER BY e.Salary DESC) AS rk
FROM Employee e
LEFT JOIN Department d ON e.departmentId = d.id) TB
WHERE rk <= 3;
```

어려움