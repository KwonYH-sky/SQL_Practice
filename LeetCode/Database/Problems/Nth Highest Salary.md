⚙[문제보기](https://leetcode.com/problems/nth-highest-salary/)



🔎문제 풀이
MySQL
```MySQL
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
 DECLARE M INT;
 SET M = N-1;
  RETURN (
      # Write your MySQL query statement below.
      SELECT DISTINCT(salary) from Employee order by salary DESC
      LIMIT 1 OFFSET M
  );
END
```
#### Function
```
CREATE FUNCTION '함수명' (
파라미터
) RETURNS 반환할 데이터타입
BEGIN
	수행할 쿼리
	RETURN 반환할 값
END
```
 - 위 방법으로 함수를 선언할 수 있다.