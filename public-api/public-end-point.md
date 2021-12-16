# Public End-Point

## User

| 이름      | Method | End-Point         |
| ------- | ------ | ----------------- |
| 로그인     | POST   | /login            |
| 로그아웃    | GET    | /logout           |
| 회원가입    | POST   | /sign-up          |
| 회원수정    | PUT    | /users/:{user-id} |
| 회원탈퇴    | DELETE | /users/:{user-id} |
| 내 정보 조회 | GET    | /userinfo         |
| 사용자 인증  | GET    | /auth             |

## Board

|            |        |                             |
| ---------- | ------ | --------------------------- |
| 카테고리 목록 조회 | GET    | /categories                 |
| 게시판 조회     | GET    | /qna/:{board\_id}           |
| 게시판 목록 조회  | GET    | /qna/list                   |
| 게시물 작성     | POST   | /qna/questions              |
| 게시물 수정     | PUT    | /qna/questions/:\[board-id} |
| 게시물 삭제     | DELETE | /qna/questions/:\[board-id} |

## Answer

|        |        |                                      |
| ------ | ------ | ------------------------------------ |
| 답변글 작성 | POST   | /qna/answer                          |
| 답변글 수정 | PUT    | /qna/answer/:\[board-id}             |
| 답변글 삭제 | DELETE | /qna/answer/:\[board-id}             |
| 답변글 채택 | PUT    | /qna/answer/best-answer/:\[board-id} |

## Like

|               |        |                                  |
| ------------- | ------ | -------------------------------- |
| 좋아요 UP \[게시글] | PUT    | /qna/questions/likes/:{board-id} |
| 좋아요 취소 \[게시글] | DELETE | /qna/questions/likes/:{board-id} |
| 좋아요 UP \[답변글] | PUT    | /qna/answers/likes/:{answer-id}  |
| 좋아요 취소 \[답변글] | DELETE | /qna/answers/likes/:{answer-id}  |
