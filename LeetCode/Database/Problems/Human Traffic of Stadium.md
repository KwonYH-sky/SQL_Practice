⚙[문제보기](https://leetcode.com/problems/human-traffic-of-stadium/)



🔎문제 풀이
MySQL
```MySQL
WITH t AS (
    SELECT t1.id, t1.visit_date, t1.people,
        id - ROW_NUMBER() OVER(ORDER BY id) AS grp 
    FROM stadium t1
    WHERE people >= 100
)

SELECT t.id, t.visit_date, t.people
FROM t
WHERE grp IN (SELECT grp FROM t GROUP BY grp HAVING COUNT(*) >=3);
```

### WITH
- WITH [ 별명 ] AS ( SUB QUERY )
- 임시테이블 또는 가상 테이블의 개념.

### ROW_NUMBER()
- 정렬 기준으로 행 번호를 매겨주는 함수


