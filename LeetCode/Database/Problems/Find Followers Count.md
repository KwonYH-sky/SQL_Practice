⚙[문제보기](https://leetcode.com/problems/find-followers-count/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT user_id, COUNT(follower_id) AS 'followers_count'
FROM Followers
GROUP BY user_id
ORDER BY 1;
```
