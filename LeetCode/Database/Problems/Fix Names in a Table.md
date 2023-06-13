⚙[문제보기](https://leetcode.com/problems/fix-names-in-a-table/)



🔎문제 풀이
MySQL
```MySQL
SELECT user_id, CONCAT(UPPER(SUBSTR(name, 1, 1)), LOWER(SUBSTR(name, 2))) AS 'name'
FROM Users
ORDER BY user_id;
```
----
## SUBSTR()
- SUBSTR('문자열 STR', '시작지점 START', '길이 LENGTH')

## UPPER()
- 대문자로 바꾸는 함수

## LOWER()
- 소문자로 바꾸는 함수