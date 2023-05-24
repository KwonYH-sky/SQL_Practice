⚙[문제보기](https://leetcode.com/problems/the-latest-login-in-2020/)



🔎문제 풀이
MySQL
```MySQL
SELECT user_id, MAX(time_stamp) AS 'last_stamp'
FROM Logins
WHERE time_stamp LIKE '2020%'
GROUP BY user_id;
```
