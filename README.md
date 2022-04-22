# spring-lcs
> Learning Community System

<br>

## Domain Model
![oline drawio](https://user-images.githubusercontent.com/76933244/164651096-f5e97479-fd1e-4c56-9257-0b6f57d22149.png)

<br>

## MSA 설계
``` 
💡 도메인 주도 설계(DDD) 의 바운디드 컨텍스트 기반 도출
```
![Untitled Diagram drawio](https://user-images.githubusercontent.com/76933244/164673114-3c798a5f-6798-4c08-99d8-3218e1f5ec13.png)


<br>

## REST API 설계

### 회원

| Service |         URI         | Verb |
|:---------:|:-------------------:|:----:|
| 회원 가입 |        /join        | POST |
| 로그인 |       /login        | POST |
| 회원 조회 |   /user/{userId}    | GET  |
| 강사 생성 |     /instructor     | POST |
| 권한 조회 | /user/{userId}/auth | GET  |
| 권한 부여 | /user/{userId}/auth | POST |


### 강의 

|  Service  |               URI                | Verb  |
|:---------:|:--------------------------------:|:-----:|
|   강의 생성   |             /lecture             | POST  |
| 강의 리스트 조회 |             /lecture             |  GET  |
| 강의 조회 |       /lecture/{lectureId}       | GET |
| 강의 공개/비공개 | /lecture/{lectureId}/open-close  | PATCH |
|   강사 매칭   |   /lecture/{lectureId}/teacher   | POST  |
|   수강 신청   | /lecture/{lectureId}/application | POST  |
|   수강 조회   |        /lecture/{userId}         | POST  |
|  컨텐츠 조회   |   /lecture/{lectureId}/content   |  GET  |
|  컨텐츠 생성   |   /lecture/{lectureId}/content   | POST  |
|   시험 등록   |    /lecture/{lectureId}/test     | POST  |
|   성적 등록   |  /lecture/{lectureId/test/score  | POST  |
|   별점 등록   |    /lecture/{lectureId}/scope    | POST  |
|   별점 조회   |    /lecture/{lectureId}/scope    |  GET  |


### 커뮤니티

| Service | URI | Verb |
|:-------:|:---:|:----:|
| 게시글 조회 | /community/ | GET  |
| 게시글 작성 | /community/post | POST |
| 게시글 관리 | /community/{postId}/open-close | PATCH |
| 댓글 조회 | /community/{postId}/comment | GET |
| 댓글 작성 | /community/{postId}/comment | POST |
| 댓글 관리 | /community/{postId}/{commentId} | PATCH |
