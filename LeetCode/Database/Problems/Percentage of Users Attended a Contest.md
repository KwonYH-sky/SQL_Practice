⚙[문제보기](https://leetcode.com/problems/percentage-of-users-attended-a-contest/)



🔎문제 풀이
MySQL
```MySQL
SELECT contest_id,
    ROUND(COUNT(DISTINCT user_id)/(SELECT COUNT(*) FROM Users)*100, 2) AS percentage
FROM Register
GROUP BY contest_id
ORDER BY 2 DESC, 1 ASC;
```