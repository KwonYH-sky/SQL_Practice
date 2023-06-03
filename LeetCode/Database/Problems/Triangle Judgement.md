⚙[문제보기](https://leetcode.com/problems/triangle-judgement/description/)



🔎문제 풀이
MySQL
```MySQL
SELECT *, IF(x+y>z AND y+z>x AND x+z>y, 'Yes', 'No') AS 'triangle'
FROM Triangle;
```
