⚙[문제보기](https://leetcode.com/problems/employee-bonus/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT name, bonus
FROM Employee E LEFT JOIN Bonus B ON E.empId = B.empId
WHERE bonus < 1000 OR bonus IS NULL;
```
OR
MySQL
```MySQL
SELECT name, bonus
FROM Employee LEFT JOIN Bonus USING(empId)
WHERE COALESCE(bonus, 0) < 1000; 
```
---
## USING()
- 두 테이블간 필드이름이 같은 경우에 사용
- JOIN 조건 사용시 ON 절에 조인 조건의 쿼리문이 긴 경우 USING를 이용해서 간략하게 작성
- ON E.empId = B.empId 와 USING(empId) 동일