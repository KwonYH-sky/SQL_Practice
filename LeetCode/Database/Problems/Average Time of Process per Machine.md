⚙[문제보기](https://leetcode.com/problems/average-time-of-process-per-machine/)



🔎문제 풀이
MySQL
```MySQL
SELECT S.machine_id, ROUND(AVG(E.timestamp-S.timestamp),3) processing_time
FROM Activity S JOIN Activity E
ON S.machine_id = E.machine_id AND S.process_id = E.process_id AND S.activity_type = 'start' AND E.activity_type = 'end'
GROUP BY 1
```
---
## SELF JOIN
- 자기 자신과 조인
- FROM 절에 동일 테이블이 두 번 이상 나타남
- 같은 테이블끼리 조인하는 것이므로 별칭(ALIAS)을 꼭 사용