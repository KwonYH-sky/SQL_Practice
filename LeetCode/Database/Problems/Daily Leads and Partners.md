⚙[문제보기](https://leetcode.com/problems/daily-leads-and-partners/description/)


🔎문제 풀이
MySQL
```MySQL
SELECT date_id, make_name, COUNT(DISTINCT lead_id) as 'unique_leads', COUNT(DISTINCT partner_id) as 'unique_partners'
FROM DailySales
GROUP BY date_id, make_name;
```
