⚙[문제보기](https://leetcode.com/problems/game-play-analysis-iv)
어려움


🔎문제 풀이
MySQL
```MySQL
WITH cte AS (
    SELECT player_id, MIN(event_date) OVER(PARTITION BY player_id) = event_date - INTERVAL 1 DAY AS is_return 
    From activity
)

SELECT ROUND(SUM(is_return)/COUNT(DISTINCT player_id), 2) AS fraction 
FROM cte;
```

