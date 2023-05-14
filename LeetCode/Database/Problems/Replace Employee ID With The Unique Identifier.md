⚙[문제보기](https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/description/)


🔎문제 풀이
MySQL
```MySQL
SELECT unique_id, name
FROM Employees E LEFT JOIN EmployeeUNI EU ON E.id = EU.id
```
