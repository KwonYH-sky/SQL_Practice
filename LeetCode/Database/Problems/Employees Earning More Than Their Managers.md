⚙[문제보기](https://leetcode.com/problems/employees-earning-more-than-their-managers/)



🔎문제 풀이
MySQL
```MySQL
SELECT a.name AS 'Employee'
FROM Employee a JOIN Employee b ON a.managerId = b.id
WHERE a.salary > b.salary;
```
