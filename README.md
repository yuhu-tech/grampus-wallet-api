## Grampus wallet App API documnet

`url: http://139.226.50.54:18080/query`

`method: POST`

`body: 请求json字符串`

`authorization: 用户授权操作，需传token`

###  Q1-1.用户信息

- ***API***

```text
query->user
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```

###  Q1-7.确认转账状态

- ***API***

```text
query->checkTrading
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  Q1-8.查询交易记录

- ***API***

```text
query->tradingRecords
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  Q1-9.查询某条交易记录

- ***API***

```text
query->tradingRecord
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  Q1-11.查询消息列表

- ***API***

```text
query->messages
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  Q1-12.查询某条消息

- ***API***

```text
query->message
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  Q1-15.查询合约信息

- ***API***

```text
query->erc20s
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  Q1-16.查询某条发布的资产

- ***API***

```text
query->assets
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```

###  M1-1.获取验证码

- ***API***

```text
mutation->sendVerificationCode
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```


###  M1-2.快速登录

- ***API***

```text
mutation->signupOrLogin
```
- ***Describe***

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
    
  - response

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
###  M1-3.刷新token

- ***API***

```text
mutation->refreshToken
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-4.添加鲸卡

- ***API***

```text
mutation->addAddress
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-5.修改鲸卡昵称

- ***API***

```text
mutation->updateAddressNickname
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-6.删除鲸卡

- ***API***

```text
mutation->deleteAddress
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-7.添加通讯录名单

- ***API***

```text
mutation->addContacter
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-8.更新通讯录名单

- ***API***

```text
mutation->updateContacter
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-9.删除通讯录名单

- ***API***

```text
mutation->deleteContacter
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-10.个人实名认证

- ***API***

```text
mutation->personalCertificate
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-11.企业实名认证

- ***API***

```text
mutation->companyCertificate
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-12.发起转账申请

- ***API***

```text
mutation->startTrading
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-13.准备转账

- ***API***

```text
mutation->prepareTrading
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-14.发布资产

- ***API***

```text
mutation->publishAssets
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-15.删除无效资产

- ***API***

```text
mutation->deleteInvaildAssets
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-16.确认消息

- ***API***

```text
mutation->checkMessage
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-17.领取认证奖励

- ***API***

```text
mutation->receiveCertificationReward
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-18.领取邀请奖励

- ***API***

```text
mutation->receiveInvitionReward
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-20.身份证识别背面信息

- ***API***

```text
mutation->resolveBackOfIdentityCard
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-21.身份证识别正面信息

- ***API***

```text
mutation->resolveFrontOfIdentityCard
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
###  M1-22.识别营业执照信息

- ***API***

```text
mutation->resolveBussinessLicense
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
  
  ```
- ***Http***

  - body
    ```text
    
    ```
    
  - response

    ```json
    
    ```
