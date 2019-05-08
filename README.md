## Grampus wallet App API documnet

`url: http://139.226.50.54:18080/query`

`method: POST`

`body: 请求json字符串`

`authorization: 用户授权操作，token`

### 1.快速登录 M1-2

- ***API***

```text
mutation->signupOrLogin
```
- ***Parameter***

```text
{
  token: "用户tocken",
  refreshToken: "更新token",
  expiredDate: "到期时间",
  user: {
    id: "用户id",
    createdAt: "",
    phoneNumber: "电话号码",
    InviterUserID: "邀请用户id",
    CountOfInvitees: "",
    addresses: {
      id: "用户地址id",
      addressString: "用户地址",
      nickname: "地址名"
    },
    contacts: {
      id: "联系人地址id",
      addressString: "联系人地址",
      nickname: "联系人备注名"
    },
    certificationStatus: "",
    certificationRewards: {
      id: "",
      createdAt: "",
      toAddress: "发送奖励地址",
      receivedAt: "接受奖励地址",
      expiredAt: "到期时间",
      txHash: "交易hash",
      rewardStatus: "奖励状态",
      rewardContent: "奖励内容",
    },
    invitionRewards: {
      id: "",
      createdAt: "",
      toAddress: "发送奖励地址",
      receivedAt: "接受奖励地址",
      expiredAt: "到期时间",
      txHash: "交易hash",
      invitee: "",
      rewardStatus: "奖励状态",
      rewardContent: "奖励内容"
    },
    assetses: {
      id: "资产id",
      createdAt: "",
      publishAddress: "发布地址",
      assetsName: "资产名",
      assetsSymbol: "资产符号",
      decimals: "小数位数",
      totalSupply: "总发送量",
      publishStatus: "发送状态",
    }
  }
}
```
- ***Graphql***

  - body 

  ```text
  mutation{
      signupOrLogin(phoneNumber: "17740657205", verificationCode: "1234", inviteCode: "") {
        token
        refreshToken
        expiredDate
        user{
          id
          createdAt
          phoneNumber
          InviterUserID
          CountOfInvitees
          addresses {
            id
          }
          contacts {
            id
          }
          certificationStatus {
            id
          }
          certificationRewards {
            id
          }
          invitionRewards {
            id
          }
          assetses {
            id
          }
        }
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  signupOrLogin(phoneNumber: \"17740657205\", verificationCode: \"1234\", inviteCode: \"\") {\n    token\n    refreshToken\n    expiredDate\n    user{\n      id\n      createdAt\n      phoneNumber\n      InviterUserID\n      CountOfInvitees\n      addresses {\n        id\n      }\n      contacts {\n        id\n      }\n      certificationStatus {\n        id\n      }\n      certificationRewards {\n        id\n      }\n      invitionRewards {\n        id\n      }\n      assetses {\n        id\n      }\n    }\n  }\n}","variables":null}
    ```
- ***Response***

    ```json
    {
      "data": {
        "signupOrLogin": {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0wN1QwNzo0NDo1OS44OThaIiwiZXhwIjoxNTU3MzIzMzU0LCJpZCI6IlkycDJaR2h1ZURFMk1EQTBjekEzTWpCcU9UTmlPV1JsYWc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQifQ.3UD5wKDokCSriaiO1SzBvAg0D9fPA6i2HbQvcxyfdkQ",
          "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0wN1QwNzo0NDo1OS44OThaIiwiZXhwIjoxNTU4MDgzMzU0LCJpZCI6IlkycDJaR2h1ZURFMk1EQTBjekEzTWpCcU9UTmlPV1JsYWc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQiLCJvbmx5X3JlZnJlc2giOiJ0cnVlIn0.0RStN9JfU-mjO07JC2eQiCm4pfHgQ2YYGlCSa-e04Yk",
          "expiredDate": "1557323354",
          "user": {
            "id": "cjvdhaqet000u0720ngvvutjr",
            "createdAt": "2019-05-07T07:34:44.744Z",
            "phoneNumber": "18721341306",
            "InviterUserID": "cjvdhiixx002e0720dyrflk1x",
            "CountOfInvitees": 3,
            "addresses": [
              {
                "id": "cjvdhl3os00330720by3dn5ei"
              },
              {
                "id": "cjvdhlfjz003e07202hs5dfce"
              }
            ],
            "contacts": [
              {
                "id": "cjvdhls2o003q0720daor9jp6"
              },
              {
                "id": "cjvdhm1x900410720umbglhs2"
              }
            ],
            "certificationStatus": {
              "id": "cjvdhnokf004i0720eaqxrev8"
            },
            "certificationRewards": null,
            "invitionRewards": null,
            "assetses": []
          }
        }
      }
    }
    ```
