## Grampus wallet App API documnet

==`url: http://139.226.50.54:18080/query`==

==`method: POST`==

==`body: 请求json字符串`==

==`header: 设置用户tocken`==

### 1.快速登录 M1-2
- API
```text
mutation->signupOrLogin
```
- body
```text
{"query":"mutation{signupOrLogin(phoneNumber:"17740657205",verificationCode:"1234") {refreshToken,token,expiredDate,user{id,phoneNumber}}}","variables":null}
```
- response
```json
{
  "data": {
    "signupOrLogin": {
      "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0wNVQwMzozNzo1OC4wNTVaIiwiZXhwIjoxNTU3ODM1MjcxLCJpZCI6IlkycDJZV1I1YWpOaU1EQXdhREEzTVRZemJHVnpNMlptWWc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQiLCJvbmx5X3JlZnJlc2giOiJ0cnVlIn0.Kce6NQgGj9LXun0U_xLpSfCB_Gs0x94OQlTAPOqluVg",
      "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0wNVQwMzozNzo1OC4wNTVaIiwiZXhwIjoxNTU3MDc1MjcxLCJpZCI6IlkycDJZV1I1YWpOaU1EQXdhREEzTVRZemJHVnpNMlptWWc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQifQ.T6DRNCKBOFybzQc2_Kn6ZZXb-UMPXZThHQqt08aAlOs",
      "expiredDate": "1557075271",
      "user": {
        "id": "cjvadyj3b000h07163les3ffb",
        "phoneNumber": "17740657205"
      }
    }
  }
}
```
