⚙[문제보기](https://leetcode.com/problems/classes-more-than-5-students/)



🔎문제 풀이
MySQL
```MySQL
SELECT class
FROM Courses
GROUP BY class
HAVING COUNT(*) >= 5;
```