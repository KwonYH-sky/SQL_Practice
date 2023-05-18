⚙[문제보기](https://leetcode.com/problems/rearrange-products-table/)


🔎문제 풀이
MySQL
```MySQL
SELECT product_id, 'store1' AS 'store', store1 AS 'price'
FROM Products
WHERE store1 IS NOT NULL

UNION
SELECT product_id, 'store2' AS 'store', store2 AS 'price'
FROM Products
WHERE store2 IS NOT NULL

UNION
SELECT product_id, 'store3' AS 'store', store3 AS 'price'
FROM Products
WHERE store3 IS NOT NULL
```

---
## UNION
- 2개 이상 테이블에 존재하는 같은 성격의 값을 하나의 쿼리로 추출
- 중복되지 않은 값만 추출 (UNION = UNION DISTINCT)

### UNION ALL
- 중복 허용하고 모든 값 추출