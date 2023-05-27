⚙[문제보기](https://leetcode.com/problems/game-play-analysis-i/)



🔎문제 풀이
MySQL
```MySQL
SELECT player_id, MIN(event_date) AS "first_login"
FROM Activity
GROUP BY player_id;
```
