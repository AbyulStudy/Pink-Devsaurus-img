# Public API 문서

## Public Access Token&#x20;

```
Cookie:pinkToken=jwtAccessToken
```

## Public HTTP Status Code

| Code | Name                  |                                |
| ---- | --------------------- | ------------------------------ |
| 200  | OK                    | \[GET] OK                      |
| 201  | Created               | \[POST] OK                     |
| 204  | NoContent             | \[PUT , DELETE] OK             |
| 400  | Bad Request           | Body의 값이 부족하거나 잘못된 값이 들어온 경우   |
| 401  | Unauthorized          | Token 이 없거나 유효기간이 만료된 경우       |
| 403  | Forbidden             | Token 이 있지만 권한이 없는 경우          |
| 404  | Not Found             | 잘못된 페이지를 들어왔거나, 잘못된 데이터를 보낸 경우 |
| 409  | Confict               | 중복 데이터가 들어온 경우                 |
| 500  | Internal Server Error | 서버에서 오류가 일어 난 경우               |

## Public Response

```
{
    "result": [data]
}
```

## Public Request

```
{
    "data_id": "data",
}
```

## Public End-Point

### User

| 이름      | Method | End-Point         |
| ------- | ------ | ----------------- |
| 로그인     | POST   | /login            |
| 로그아웃    | GET    | /logout           |
| 회원가입    | POST   | /sign-up          |
| 회원수정    | PUT    | /users/:{user-id} |
| 회원탈퇴    | DELETE | /users/:{user-id} |
| 내 정보 조회 | GET    | /userinfo         |
| 사용자 인증  | GET    | /auth             |

### Board

| 이름         | Method | End-Point                   |
| ---------- | ------ | --------------------------- |
| 카테고리 목록 조회 | GET    | /categories                 |
| 게시판 조회     | GET    | /qna/:{board\_id}           |
| 게시판 목록 조회  | GET    | /qna/list                   |
| 게시물 작성     | POST   | /qna/questions              |
| 게시물 수정     | PUT    | /qna/questions/:\[board-id} |
| 게시물 삭제     | DELETE | /qna/questions/:\[board-id} |

### Answer

| 이름     | Method | End-Point                            |
| ------ | :----: | ------------------------------------ |
| 답변글 작성 |  POST  | /qna/answer                          |
| 답변글 수정 |   PUT  | /qna/answer/:\[board-id}             |
| 답변글 삭제 | DELETE | /qna/answer/:\[board-id}             |
| 답변글 채택 |   PUT  | /qna/answer/best-answer/:\[board-id} |

### Like

| 이름            | Method | End-Point                        |
| ------------- | :----: | -------------------------------- |
| 좋아요 UP \[게시글] |   PUT  | /qna/questions/likes/:{board-id} |
| 좋아요 취소 \[게시글] | DELETE | /qna/questions/likes/:{board-id} |
| 좋아요 UP \[답변글] |   PUT  | /qna/answers/likes/:{answer-id}  |
| 좋아요 취소 \[답변글] | DELETE | /qna/answers/likes/:{answer-id}  |



