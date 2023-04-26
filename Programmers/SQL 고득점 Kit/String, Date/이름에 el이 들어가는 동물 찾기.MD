⚙[문제보기](https://school.programmers.co.kr/learn/courses/30/lessons/59047)


🔎문제 풀이
MySQL
```MySQL
SELECT ANIMAL_ID, NAME FROM ANIMAL_INS
WHERE NAME LIKE '%el%' AND ANIMAL_TYPE = 'Dog'
ORDER BY NAME ASC;
```
