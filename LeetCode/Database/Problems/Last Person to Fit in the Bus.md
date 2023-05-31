⚙[문제보기](https://leetcode.com/problems/last-person-to-fit-in-the-bus/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT Q1.person_name
FROM Queue Q1 JOIN Queue Q2 ON Q1.turn >= Q2.turn
GROUP BY Q1.turn
HAVING SUM(Q2.weight) <= 1000
ORDER BY SUM(Q2.weight) DESC
LIMIT 1;
```
