⚙[문제보기](https://leetcode.com/problems/actors-and-directors-who-cooperated-at-least-three-times/)



🔎문제 풀이
MySQL
```MySQL
SELECT actor_id, director_id
FROM ActorDirector
GROUP BY actor_id, director_id
HAVING COUNT(*) > 2;
```
