⚙[문제보기](https://leetcode.com/problems/big-countries/)



🔎문제 풀이
MySQL
```MySQL
SELECT name, population, area
FROM World
WHERE area >= 3000000 OR population >= 25000000;
```
