⚙[문제보기](https://leetcode.com/problems/rising-temperature)



🔎문제 풀이
MySQL
```MySQL
SELECT w1.id
FROM Weather AS w1 , Weather AS w2
WHERE w1.Temperature > w2.Temperature AND DATEDIFF(w1.recordDate , w2.recordDate) = 1
```