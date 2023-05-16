⚙[문제보기](https://leetcode.com/problems/invalid-tweets/description/)


🔎문제 풀이
MySQL
```MySQL
SELECT tweet_id FROM Tweets
WHERE CHAR_LENGTH(content) > 15;
```


---
## LENGTH()
- BYTE값으로 띄어쓰기를 포함해 길이를 반환함.
- 영문(1byte), 한글(3byte)로 반환함

## CHAR_LENGTH()
- 문자 개수를 반환함.