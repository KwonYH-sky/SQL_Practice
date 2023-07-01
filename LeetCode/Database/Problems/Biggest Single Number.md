⚙[문제보기](https://leetcode.com/problems/biggest-single-number/)



🔎문제 풀이
MySQL
```MySQL
SELECT MAX(num) AS num
FROM (
  SELECT num
  FROM MyNumbers
  GROUP BY num
  HAVING COUNT(*) < 2
) TB;
```

OR

MySQL
```MySQL
SELECT(
  SELECT num
  FROM MyNumbers
  GROUP BY num
  HAVING COUNT(*) = 1
  ORDER BY num DESC LIMIT 1
) AS num;
```

아래가 300ms 더 빠름