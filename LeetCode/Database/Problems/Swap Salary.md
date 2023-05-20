⚙[문제보기](https://leetcode.com/problems/swap-salary/description/)
SELECT문 사용하지 않고 UPDATE문으로 작성하기


🔎문제 풀이
MySQL
```MySQL
UPDATE Salary 
SET sex = IF(sex = 'm', 'f', 'm');
```

---
## UPDATE
- UPDATE 문을 사용하여 레코드의 내용을 수정
```
UPDATE 테이블이름

SET 필드이름1=데이터값1, 필드이름2=데이터값2, ...

WHERE 필드이름=데이터값
```