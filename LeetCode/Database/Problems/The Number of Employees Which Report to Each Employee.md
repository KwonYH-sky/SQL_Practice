⚙[문제보기](https://leetcode.com/problems/the-number-of-employees-which-report-to-each-employee)



🔎문제 풀이
MySQL
```MySQL
SELECT e1.employee_id, e1.name, COUNT(*) reports_count, ROUND(AVG(e2.age), 0) average_age
FROM Employees e1 JOIN Employees e2
ON e1.employee_id = e2.reports_to
GROUP BY 1
ORDER BY 1;
```