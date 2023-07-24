⚙[문제보기](https://leetcode.com/problems/find-users-with-valid-e-mails//)



🔎문제 풀이
MySQL
```MySQL
SELECT * 
FROM Users
WHERE mail REGEXP '^[a-zA-Z][a-zA-Z0-9_.-]*@leetcode[.]com$';
```

### REGEXP
- 정규표현식을 이용하여 검색하게 해줄 수 있게함
- 정규표현식을 활용하여 기본 연산자보다 복잡한 문자열 조건을 걸어 데이터를 검색할 수 있음