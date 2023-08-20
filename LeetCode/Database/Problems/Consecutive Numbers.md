⚙[문제보기](https://leetcode.com/problems/consecutive-numbers/)



🔎문제 풀이
MySQL
```MySQL
SELECT DISTINCT num AS 'ConsecutiveNums' 
FROM Logs
WHERE (id + 1, num) IN (SELECT * FROM Logs) AND (id + 2, num) IN (SELECT * FROM Logs);
```

```MySQL
WITH cte AS (
    SELECT num,
    LEAD(num,1) OVER() num1,
    LEAD(num,2) OVER() num2
    FROM Logs

)

SELECT DISTINCT num ConsecutiveNums FROM cte WHERE (num=num1) AND (num=num2)
```

### LEAD()
- 현재 행 기준 이전 행 값을 가져오는 함수

### LEG()
- 현재 행 기준 다음 행 값을 가져오는 함수