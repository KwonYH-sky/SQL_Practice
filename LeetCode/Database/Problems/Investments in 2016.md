⚙[문제보기](https://leetcode.com/problems/investments-in-2016/)



🔎문제 풀이
MySQL
```MySQL
# 하나 이상의 다른 보험계약자와 동일한 tiv_2015 값을 갖아야 함
# 동일한 위치가 아니여야함
SELECT ROUND(SUM(tiv_2016), 2) AS tiv_2016
FROM (
  SELECT *,
        COUNT(*) OVER(PARTITION BY tiv_2015) CN1,
        COUNT(*) OVER(PARTITION BY lat, lon) CN2
  FROM Insurance
) TB
WHERE CN1 >=2 AND CN2 = 1;
```