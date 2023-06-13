⚙[문제보기](https://leetcode.com/problems/project-employees-i/)



🔎문제 풀이
MySQL
```MySQL
SELECT project_id, ROUND(AVG(experience_years), 2) AS 'average_years'
FROM Project P JOIN Employee E ON P.employee_id = E.employee_id
GROUP BY project_id;
```
