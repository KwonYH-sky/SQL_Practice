⚙[문제보기](https://leetcode.com/problems/exchange-seats/)



🔎문제 풀이
MySQL
```MySQL
SELECT CASE 
        WHEN id % 2 = 0 THEN id-1
        WHEN id % 2 = 1 AND id < (SELECT COUNT(*) FROM Seat) THEN id + 1
        ELSE id
       END AS 'id',
       student
FROM Seat
ORDER BY id;
```
