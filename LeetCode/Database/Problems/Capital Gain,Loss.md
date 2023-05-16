⚙[문제보기](https://leetcode.com/problems/capital-gainloss/)


🔎문제 풀이
MySQL
```MySQL
SELECT stock_name, SUM(IF(operation="Buy", -price, price)) capital_gain_loss
FROM Stocks
GROUP BY stock_name;
```
