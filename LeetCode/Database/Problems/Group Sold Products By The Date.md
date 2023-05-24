⚙[문제보기](https://leetcode.com/problems/group-sold-products-by-the-date/)



🔎문제 풀이
MySQL
```MySQL
SELECT sell_date, COUNT(DISTINCT product) as 'num_sold',
    GROUP_CONCAT(DISTINCT product ORDER BY product ASC) products
FROM Activities
GROUP BY sell_date
ORDER BY sell_date ASC;
```
----
## GROUP_CONCAT()
- 특정컬럼의 각 결과값을 하나의 가로열(ROW)로 표시
- SEPARATOR로 각 칼럼 구분자를 지정할 수 있음(기본값으로 ',')
- ORDER BY로 정렬 및 DISTINCT로 중복값 제거 가능
```
GROUP_CONCAT(칼럼 ORDER BY 칼럼 SEPARATOR '|')
```

*출력값* -  `갈럼1 | 칼럼2 | 칼럼3 | ....`