⚙[문제보기](https://leetcode.com/problems/employees-with-missing-information/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT T.employee_id
FROM  
  (SELECT * FROM Employees LEFT JOIN Salaries USING(employee_id)
   UNION 
   SELECT * FROM Employees RIGHT JOIN Salaries USING(employee_id))
AS T
WHERE T.salary IS NULL OR T.name IS NULL
ORDER BY employee_id;
```

---
## MySQL에 FULL JOIN
- MySQL에서는 FULL JOIN이 지원되지않음
- LEFT JOIN과 RIGHT JOIN을 UNION하여 구현 가능