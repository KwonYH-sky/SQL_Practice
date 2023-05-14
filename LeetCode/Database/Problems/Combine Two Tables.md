⚙[문제보기](https://leetcode.com/problems/combine-two-tables/description/)


🔎문제 풀이
MySQL
```MySQL
SELECT firstName, lastName, city, state
FROM Person P LEFT JOIN Address A ON P.personId = A.personId
```
