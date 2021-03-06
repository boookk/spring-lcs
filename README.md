# spring-lcs
> Learning Community System

<br>

## Domain Model
![oline drawio](https://user-images.githubusercontent.com/76933244/164651096-f5e97479-fd1e-4c56-9257-0b6f57d22149.png)

<br>

## MSA ์ค๊ณ
``` 
๐ก ๋๋ฉ์ธ ์ฃผ๋ ์ค๊ณ(DDD) ์ ๋ฐ์ด๋๋ ์ปจํ์คํธ ๊ธฐ๋ฐ ๋์ถ
```
![Untitled Diagram drawio](https://user-images.githubusercontent.com/76933244/164673114-3c798a5f-6798-4c08-99d8-3218e1f5ec13.png)


<br>

## REST API ์ค๊ณ

### ํ์

| Service |         URI         | Verb |
|:---------:|:-------------------:|:----:|
| ํ์ ๊ฐ์ |        /join        | POST |
| ๋ก๊ทธ์ธ |       /login        | POST |
| ํ์ ์กฐํ |   /user/{userId}    | GET  |
| ๊ฐ์ฌ ์์ฑ |     /instructor     | POST |
| ๊ถํ ์กฐํ | /user/{userId}/auth | GET  |
| ๊ถํ ๋ถ์ฌ | /user/{userId}/auth | POST |


### ๊ฐ์ 

|  Service  |               URI                | Verb  |
|:---------:|:--------------------------------:|:-----:|
|   ๊ฐ์ ์์ฑ   |             /lecture             | POST  |
| ๊ฐ์ ๋ฆฌ์คํธ ์กฐํ |             /lecture             |  GET  |
| ๊ฐ์ ์กฐํ |       /lecture/{lectureId}       | GET |
| ๊ฐ์ ๊ณต๊ฐ/๋น๊ณต๊ฐ | /lecture/{lectureId}/open-close  | PATCH |
|   ๊ฐ์ฌ ๋งค์นญ   |   /lecture/{lectureId}/teacher   | POST  |
|   ์๊ฐ ์ ์ฒญ   | /lecture/{lectureId}/application | POST  |
|   ์๊ฐ ์กฐํ   |        /lecture/{userId}         | GET  |
|  ์ปจํ์ธ  ์กฐํ   |   /lecture/{lectureId}/content   |  GET  |
|  ์ปจํ์ธ  ์์ฑ   |   /lecture/{lectureId}/content   | POST  |
|   ์ํ ๋ฑ๋ก   |    /lecture/{lectureId}/test     | POST  |
|   ์ฑ์  ๋ฑ๋ก   |  /lecture/{lectureId/test/score  | POST  |
|   ๋ณ์  ๋ฑ๋ก   |    /lecture/{lectureId}/scope    | POST  |
|   ๋ณ์  ์กฐํ   |    /lecture/{lectureId}/scope    |  GET  |


### ์ปค๋ฎค๋ํฐ

| Service | URI | Verb |
|:-------:|:---:|:----:|
| ๊ฒ์๊ธ ์กฐํ | /community/ | GET  |
| ๊ฒ์๊ธ ์์ฑ | /community/post | POST |
| ๊ฒ์๊ธ ๊ด๋ฆฌ | /community/{postId}/open-close | PATCH |
| ๋๊ธ ์กฐํ | /community/{postId}/comment | GET |
| ๋๊ธ ์์ฑ | /community/{postId}/comment | POST |
| ๋๊ธ ๊ด๋ฆฌ | /community/{postId}/{commentId} | PATCH |
