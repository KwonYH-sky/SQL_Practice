⚙[문제보기](https://leetcode.com/problems/friend-requests-ii-who-has-the-most-friends/)



🔎문제 풀이
MySQL
```MySQL
SELECT id, COUNT(*) AS 'num' 
FROM (
  (SELECT requester_id id FROM RequestAccepted)
  UNION ALL
  (SELECT accepter_id id FROM RequestAccepted)
) TB
GROUP BY id 
ORDER BY num DESC
LIMIT 1;
```

어려움