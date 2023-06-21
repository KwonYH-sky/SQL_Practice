⚙[문제보기](https://leetcode.com/problems/rank-scores/)



🔎문제 풀이
MySQL
```MySQL
SELECT score, DENSE_RANK() OVER(ORDER BY score DESC) as "rank"
FROM Scores;
```

---
## RANK/DENSE_RANK/ROW_NUMBER
- 모두 특정 열의 값에 대해 순위를 매기는 함수이다.
- RANK()는 공동 순위만큼 건너뜀 (ex: 1,2,2,4 ...)
- DENSE_RANK()는 공동 순위를 뛰어넘지 않음 (ex: 1,2,2,3 ...)
- ROW_NUMBER() 공동 순위를 무시함 (ex: 1,2,3,4 ...)
- OVER()와 함께 쓰인다.

## 윈도우 함수 (Window Function)
- 행과 행 간의 관계를 정의하기 위해 제공되는 함수이다.
 ```
 FUNCTION(column) OVER(PARITION BY column ORDER BY column)
 ```
- FUNCTION : COUNT, SUM, RANK 등 사용할 함수
- PARTITION BY : 컬럼을 기준으로 테이블을 그룹화한다. 생략하면 테이블 전체를 하나의 그룹으로 처리한다.
- ORDER BY : 컬럼을 기준으로 정렬한다.

