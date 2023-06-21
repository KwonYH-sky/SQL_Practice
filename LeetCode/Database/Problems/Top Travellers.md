⚙[문제보기](https://leetcode.com/problems/top-travellers/)



🔎문제 풀이
MySQL
```MySQL
SELECT DISTINCT name, COALESCE(SUM(distance) OVER(PARTITION BY U.id), 0) AS 'travelled_distance'
FROM Users U LEFT JOIN Rides R ON U.id = R.user_id
ORDER BY travelled_distance DESC, name;
```