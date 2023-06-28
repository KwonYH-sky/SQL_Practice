⚙[문제보기](https://leetcode.com/problems/calculate-special-bonus/)



🔎문제 풀이
MySQL
```MySQL
SELECT employee_id,
    IF(employee_id%2 != 0 AND name NOT LIKE 'M%', salary, 0)  AS 'bonus'
FROM Employees
ORDER BY 1;
```