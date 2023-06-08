⚙[문제보기](https://leetcode.com/problems/queries-quality-and-percentage/)



🔎문제 풀이
MySQL
```MySQL
SELECT query_name, ROUND(AVG(rating/position), 2) AS 'quality',
  ROUND(AVG(rating < 3)*100, 2) AS 'poor_query_percentage'
FROM Queries
GROUP BY query_name;
```
