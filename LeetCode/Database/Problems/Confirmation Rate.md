⚙[문제보기](https://leetcode.com/problems/confirmation-rate/)



🔎문제 풀이
MySQL
```MySQL
SELECT S.user_id, 
    COALESCE(ROUND(SUM(C.action='confirmed')/COUNT(S.user_id), 2),0) AS 'confirmation_rate'
FROM Signups S LEFT JOIN Confirmations C ON S.user_id = C.user_id
GROUP BY S.user_id
```