⚙[문제보기](https://leetcode.com/problems/delete-duplicate-emails/)

SELECT문 사용하지 않고 DELETE문 사용하기


🔎문제 풀이
MySQL
```MySQL
DELETE P1
FROM Person P1, Person P2
WHERE P1.email = P2.email AND P1.id > P2.id;
```

---
## DELETE
 - DELETE 문을 사용하여 테이블의 레코드를 삭제
 - 문법
    ```
    DELETE FROM 테이블이름 
    WHERE 필드이름=데이터값
    ```
- DELETE 문은 해당 테이블에서 WHERE 절의 조건을 만족하는 레코드만을 삭제한다.
- 즉, 테이블에서 명시된 필드와, 그 값이 일치하는 레코드만을 삭제한다.
