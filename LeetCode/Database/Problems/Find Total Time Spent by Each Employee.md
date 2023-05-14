⚙[문제보기](https://leetcode.com/problems/find-total-time-spent-by-each-employee/description/)


🔎문제 풀이
MySQL
```MySQL
SELECT event_day as 'day', emp_id, SUM(out_time - in_time) as 'total_time'
FROM Employees
GROUP BY event_day, emp_id
```
