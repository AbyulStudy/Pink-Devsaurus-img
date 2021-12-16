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
