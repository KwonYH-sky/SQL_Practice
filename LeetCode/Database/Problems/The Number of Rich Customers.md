⚙[문제보기](https://leetcode.com/problems/the-number-of-rich-customers/)



🔎문제 풀이
MySQL
```MySQL
SELECT COUNT(customer_id) rich_count
FROM (
  SELECT DISTINCT customer_id FROM Store
  WHERE amount > 500
) T1;
```

```MySQL
SELECT COUNT(DISTINCT customer_id) rich_count
FROM Store
WHERE amount > 500;
```