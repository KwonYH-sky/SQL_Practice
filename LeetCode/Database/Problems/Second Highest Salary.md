⚙[문제보기](https://leetcode.com/problems/product-sales-analysis-iii)



🔎문제 풀이
MySQL
```MySQL
SELECT MAX(salary) AS SecondHighestSalary
FROM Employee
WHERE salary < (SELECT MAX(salary) FROM Employee)
```

OR

```MySQL
SELECT MAX(salary) AS SecondHighestSalary
FROM (
  SELECT *, DENSE_RANK() OVER(ORDER BY salary DESC) AS rank_desc
  FROM Employee
) T1
WHERE rank_desc = 2;
```