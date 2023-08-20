⚙[문제보기](https://leetcode.com/problems/movie-rating)



🔎문제 풀이
MySQL
```MySQL
(
  SELECT name AS 'results'
  FROM MovieRating r JOIN Users u ON r.user_id = u.user_id
  GROUP BY r.user_id
  ORDER BY COUNT(*) DESC, 1
  LIMIT 1
)
UNION ALL
(
  SELECT title AS 'results'
  FROM MovieRating r JOIN Movies m ON r.movie_id = m.movie_id
  WHERE created_at LIKE '2020-02%'
  GROUP BY r.movie_id
  ORDER BY AVG(rating) DESC, 1
  LIMIT 1
)
```