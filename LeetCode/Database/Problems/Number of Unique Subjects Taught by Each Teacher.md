⚙[문제보기](https://leetcode.com/problems/number-of-unique-subjects-taught-by-each-teacher/description/)


🔎문제 풀이
MySQL
```MySQL
SELECT teacher_id, COUNT(DISTINCT subject_id) as 'cnt'
FROM Teacher
GROUP BY teacher_id;
```
