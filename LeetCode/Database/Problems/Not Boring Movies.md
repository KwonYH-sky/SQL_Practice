⚙[문제보기](https://leetcode.com/problems/not-boring-movies/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT id, movie, description, rating
FROM Cinema
WHERE description != 'boring' AND id%2 = 1
ORDER BY rating DESC;
```
