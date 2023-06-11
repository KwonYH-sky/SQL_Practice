⚙[문제보기](https://leetcode.com/problems/students-and-examinations/)



🔎문제 풀이
MySQL
```MySQL
SELECT S.student_id, S.student_name, Sj.subject_name, COUNT(E.subject_name) AS 'attended_exams'
FROM Students S 
  JOIN Subjects Sj
    LEFT JOIN Examinations E   
  ON S.student_id = E.student_id AND Sj.subject_name = E.subject_name
GROUP BY S.student_id, Sj.subject_name
ORDER BY student_id, subject_name;
```
