⚙[문제보기](https://leetcode.com/problems/article-views-i/)



🔎문제 풀이
MySQL
```MySQL
SELECT author_id AS "id"
FROM Views
WHERE author_id = viewer_id
GROUP BY author_id
ORDER BY id;
```
