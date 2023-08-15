⚙[문제보기](https://leetcode.com/problems/employees-whose-manager-left-the-company/)



🔎문제 풀이
MySQL
```MySQL
SELECT e1.employee_id
FROM Employees e1 LEFT JOIN Employees e2
ON e1.manager_id = e2.employee_id 
WHERE e2.employee_id IS NULL AND e1.manager_id IS NOT NULL
AND e1.salary < 30000
ORDER BY 1;
```

```MySQL
SELECT employee_id FROM Employees
WHERE manager_id NOT IN (SELECT employee_id FROM Employees)
AND salary < 30000
ORDER BY 1;
```