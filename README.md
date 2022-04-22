# spring-lcs
> Learning Community System

<br>

## Domain Model
![oline drawio](https://user-images.githubusercontent.com/76933244/164609693-e24f4285-f808-456a-a90f-7f1b4fa4a9d3.png)

<br>

## MSA 설계
``` 
💡 도메인 주도 설계(DDD) 의 바운디드 컨텍스트 기반 도출
```
### 회원 서비스
### 강의 서비스
### 커뮤니티 서비스

<br>

## REST API 설계

### 회원

| Service |           URI            | Verb |
|:---------:|:------------------------:|:----:|
| 회원 가입 |      /members/join       | POST |
| 로그인 |      /members/login      | POST |
| 회원 조회 |      /members/{id}       | GET  |
| 강사 생성 | /members/join/instructor | POST |
| 권한 조회 |    /members/auth/{id}    | GET  |
| 권한 부여 |    /members/auth/{id}    | POST |


### 강의 

|  Service  |            URI             | Verb |
|:---------:|:--------------------------:|:----:|
|   강의 생성   |      /lecture/produce      | POST |
| 전체 강의 조회  |         /lecture/          | GET  |
| 강의 공개/비공개 | /lecture/{강의id}/open-close | POST |
|   강사 매칭   |  /lecture/{강의id}/teacher   | POST |

