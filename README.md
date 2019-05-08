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
user: {
  id: "",
  createdAt: "创建时间",
  phoneNumber: "电话号码",
  InviterUserID: "邀请人id",
  CountOfInvitees: "邀请用户数量",
  addresses: {
    id: "",
    addressString: "用户地址",
    nickname: "昵称"
  },
  contacts: {
    id: "",
    addressString: "联系人地址",
    nickname: "昵称"
  },
  certificationStatus: {
    id: "",
    createdAt: "创建时间",
    certType: "证件类型",
    certStatus: "认证状态",
    expiredAt: "失效时间",
    submitAt: "提交时间",
    auditAt: "审核时间",
    submitMark: "提交备注",
    auditMark: "审核备注",
    personalCertificationInfo: {
      id: "",
      email: "认证邮箱",
      img1URL: "身份证背面图片url",
      img2URL: "身份证正面图片url",
      identityCardInfo: {
        id: "",
        clientIDNo: "身份证号",
        name: "姓名",
        sex: "性别",
        ethnicity: "民族",
        birth: "出生日期",
        residentialAddress: "居住地",
        authority: "",
        issueDate: "签发日期",
        invalidDate: "无效日期"
      }
    },
    companyCertificationInfo: {
      id: "",
      contacter: "联系人",
      phoneNumberOfContacter: "联系人手机号",
      email: "认证邮箱",
      additionalAuthentication: "附加认证",
      accountName: "银行开户名",
      corporateAccountOfDepositBank: "对公账户开户行",
      corporateAccountNo: "对公账户账号",
      img1URL: "营业执照图片url",
      img2URL: "身份证背面图片url",
      img3URL: "身份证正面图片url",
      identityCardInfo: {
        id: "",
        clientIDNo: "身份证号",
        name: "姓名",
        sex: "性别",
        ethnicity: "民族",
        birth: "出生日期",
        residentialAddress: "居住地",
        authority: "",
        issueDate: "签发日期",
        invalidDate: "无效日期"
      },
      bussinessLicenseInfo: {
        id: "",
        registrationNo: "证件编号",
        unifiedSocialCreditCode: "统一社会信用代码",
        enterpriseName: "名称",
        typeOfEnterprise: "类型",
        residence: "住所",
        legalRepresentative: "法定代表人",
        registeredCapital: "注册资本",
        dateOfEstablishment: "成立日期",
        termOfBusiness: "营业期限",
        scopeOfBusiness: "经营范围"
      }
    }
  },
  certificationRewards: {
    id: "",
    createdAt: "创建时间",
    toAddress: "发送奖励地址",
    receivedAt: "接收奖励地址",
    expiredAt: "到期时间",
    txHash: "交易hash",
    rewardStatus: "奖励状态",
    rewardContent: "奖励内容",
  },
  invitionRewards: {
    id: "",
    createdAt: "创建时间",
    toAddress: "发送奖励地址",
    receivedAt: "接受奖励地址",
    expiredAt: "到期时间",
    txHash: "交易hash",
    inviteeUserID: "受邀者",
    rewardStatus: "奖励状态",
    rewardContent: "奖励内容"
  },
  assetses: {
    id: "",
    createdAt: "创建时间",
    publishAddress: "发布地址",
    assetsName: "资产名",
    assetsSymbol: "资产符号",
    decimals: "小数位数",
    totalSupply: "总发送量",
    publishStatus: "发送状态",
  }
}
```
- ***Graphql***

  - body 

  ```text
  {
      user {
        id
        phoneNumber
        createdAt
        InviterUserID
        CountOfInvitees
        addresses {
          id
          nickname
          addressString
        }
        contacts {
          id
          nickname
          addressString
        }
        certificationStatus {
          id
          certType
          certStatus
          expiredAt
          submitAt
          auditAt
          createdAt
          submitMark
          auditMark
          personalCertificationInfo {
            id
            email
            img1URL
            img2URL
            identityCardInfo {
              id
              clientIDNo
              name
              sex
              ethnicity
              birth
              residentialAddress
              authority
              issueDate
              invalidDate
            }
          }
          companyCertificationInfo {
            id
            contacter
            phoneNumberOfContacter
            email
            additionalAuthentication
            accountName
            corporateAccountOfDepositBank
            corporateAccountNo
            img1URL
            img2URL
            img3URL
            identityCardInfo {
              id
              clientIDNo
              name
              sex
              ethnicity
              birth
              residentialAddress
              authority
              issueDate
              invalidDate
            }
            bussinessLicenseInfo{
              id
              registrationNo
              unifiedSocialCreditCode
              enterpriseName
              typeOfEnterprise
              residence
              legalRepresentative
              registeredCapital
              dateOfEstablishment
              termOfBusiness
              scopeOfBusiness
            }
          }
        }
      }
    }
  
  ```
- ***Http***

  - body
    ```text
    {"query":"{\n  user {\n    id\n    phoneNumber\n    createdAt\n    InviterUserID\n    CountOfInvitees\n    addresses {\n      id\n      nickname\n      addressString\n    }\n    contacts {\n      id\n      nickname\n      addressString\n    }\n    certificationStatus {\n      id\n      certType\n      certStatus\n      expiredAt\n      submitAt\n      auditAt\n      createdAt\n      submitMark\n      auditMark\n      personalCertificationInfo {\n        id\n        email\n        img1URL\n        img2URL\n        identityCardInfo {\n          id\n          clientIDNo\n          name\n          sex\n          ethnicity\n          birth\n          residentialAddress\n          authority\n          issueDate\n          invalidDate\n        }\n      }\n      companyCertificationInfo {\n        id\n        contacter\n        phoneNumberOfContacter\n        email\n        additionalAuthentication\n        accountName\n        corporateAccountOfDepositBank\n        corporateAccountNo\n        img1URL\n        img2URL\n        img3URL\n        identityCardInfo {\n          id\n          clientIDNo\n          name\n          sex\n          ethnicity\n          birth\n          residentialAddress\n          authority\n          issueDate\n          invalidDate\n        }\n        bussinessLicenseInfo{\n          id\n          registrationNo\n          unifiedSocialCreditCode\n          enterpriseName\n          typeOfEnterprise\n          residence\n          legalRepresentative\n          registeredCapital\n          dateOfEstablishment\n          termOfBusiness\n          scopeOfBusiness\n        }\n      }\n    }\n  }\n}","variables":null,"operationName":""}
    ```
    
  - response

    ```json
    {
      "data": {
        "user": {
          "id": "cjvenwfgf00170780jh489frg",
          "phoneNumber": "18721341306",
          "createdAt": "2019-05-08T03:27:20.878Z",
          "InviterUserID": "cjvetylgo00f207808gjvsba8",
          "CountOfInvitees": 2,
          "addresses": [
            {
              "id": "cjvenwroi001i0780y5mvrxs0",
              "nickname": "鲸卡1",
              "addressString": "0x14ca04ff85747def87d6c6c566db84cc24e4643b"
            },
            {
              "id": "cjvenwz0i001t0780x1kyh1qc",
              "nickname": "鲸卡2",
              "addressString": "0x349118dd4764b6335055582949a24a1d76ddad15"
            }
          ],
          "contacts": [
            {
              "id": "cjvenx6pw00250780ufu7k3kg",
              "nickname": "朋友1",
              "addressString": "0x31e9a02b34d54061ac98eacba7cb214fbd392004"
            },
            {
              "id": "cjvenxdld002g07802xry4w4a",
              "nickname": "朋友2",
              "addressString": "0x619f889c5699394b9c5033bc85028eb4af11faa1"
            }
          ],
          "certificationStatus": {
            "id": "cjveny46h002s07807xxfkxmq",
            "certType": 0,
            "certStatus": 1,
            "expiredAt": "2019-05-06T03:28:13.978Z",
            "submitAt": "2019-05-07T03:28:24.383Z",
            "auditAt": "2019-05-08T03:28:26.768Z",
            "createdAt": "2019-05-08T03:28:39.593Z",
            "submitMark": "备注文字",
            "auditMark": "备注文字",
            "personalCertificationInfo": {
              "id": "cjvenyjl800340780c87xd12o",
              "email": "1547841257@qq.com",
              "img1URL": "/a/b/c",
              "img2URL": "/b/c/d",
              "identityCardInfo": {
                "id": "cjveo166m003o0780lk4lodis",
                "clientIDNo": "350642199705056624",
                "name": "陈五",
                "sex": 1,
                "ethnicity": "汉",
                "birth": "19970505",
                "residentialAddress": "上海市徐汇区徐家汇街道",
                "authority": "上海市徐汇区公安局",
                "issueDate": "20130710",
                "invalidDate": "20230709"
              }
            },
            "companyCertificationInfo": {
              "id": "cjveo2w4b004f0780e9cnmbgf",
              "contacter": "张三",
              "phoneNumberOfContacter": "1577874598",
              "email": "2547121475@qq.com",
              "additionalAuthentication": "企业对公账户认证",
              "accountName": "李四",
              "corporateAccountOfDepositBank": "上海支行",
              "corporateAccountNo": "1045788436951235",
              "img1URL": "/a/b/c",
              "img2URL": "/b/f/g",
              "img3URL": "/c/s/f",
              "identityCardInfo": {
                "id": "cjveo166m003o0780lk4lodis",
                "clientIDNo": "350642199705056624",
                "name": "陈五",
                "sex": 1,
                "ethnicity": "汉",
                "birth": "19970505",
                "residentialAddress": "上海市徐汇区徐家汇街道",
                "authority": "上海市徐汇区公安局",
                "issueDate": "20130710",
                "invalidDate": "20230709"
              },
              "bussinessLicenseInfo": {
                "id": "cjveo1sqv00400780uk3o9k3i",
                "registrationNo": "51249546385231385226",
                "unifiedSocialCreditCode": "75213698533",
                "enterpriseName": "上海娱乐有限公司",
                "typeOfEnterprise": "有限责任公司(国内合资)",
                "residence": "上海市金山区金山路105号201室",
                "legalRepresentative": "赵六",
                "registeredCapital": "人民币50,000万元整",
                "dateOfEstablishment": "2011年10月15日",
                "termOfBusiness": "2011年10月15日至2021年10月14日",
                "scopeOfBusiness": "经营各种服务"
              }
            }
          }
        }
      }
    }
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
{
  message: {
    id: ""
    fromUserID: "消息发送者"
    toUserID: "消息接受者"
    sendAt: "发送时间"
    checkedAt: "确认时间"
    checkStatus: "确认状态"
    messageContent: {
      id: ""
      createdAt: "创建时间"
      content: "内容"
    }
  }
}
```
- ***Graphql***

  - body 

  ```text
    query{
      messages(limit: 10, skip: 0) {
        id
        toUser
        sendAt
        checkedAt
        checkStatus
        messageContent{
          id
          createdAt
          fromUser
          toUser
          content
        }
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"query{\n  messages(limit: 10, skip: 0) {\n    id\n    toUser\n    sendAt\n    checkedAt\n    checkStatus\n    messageContent{\n      id\n      createdAt\n      fromUser\n      toUser\n      content\n    }\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "messages": [
          {
            "id": "cjveo63w2006p078073k9up6j",
            "toUser": "cjvenwfgf00170780jh489frg",
            "sendAt": "2019-05-06T03:34:41.477Z",
            "checkedAt": "2019-05-07T00:31:42.107Z",
            "checkStatus": 1,
            "messageContent": {
              "id": "cjveo6m8s007007809mhjxuie",
              "createdAt": "2019-05-08T03:35:16.252Z",
              "fromUser": "\"cjvet3hsr00900780bcvgthdm\"",
              "toUser": "\"cjvetylgo00f207808gjvsba8\"",
              "content": "内容"
            }
          },
          {
            "id": "cjveu1fvg00gm0780e22oc6w7",
            "toUser": "cjvenwfgf00170780jh489frg",
            "sendAt": "2019-05-04T06:18:50.969Z",
            "checkedAt": "2019-05-08T06:18:55.390Z",
            "checkStatus": 1,
            "messageContent": {
              "id": "cjveu0uy100ga0780vja3wys3",
              "createdAt": "2019-05-08T06:18:45.288Z",
              "fromUser": "\"cjvet3hsr00900780bcvgthdm\"",
              "toUser": "\"cjvetylgo00f207808gjvsba8\"",
              "content": "内容"
            }
          }
        ]
      }
    }
    ```
###  Q1-12.查询某条消息

- ***API***

```text
query->message
```
- ***Describe***

```text
{
  message: {
    id: ""
    fromUserID: "消息发送者"
    toUserID: "消息接受者"
    sendAt: "发送时间"
    checkedAt: "确认时间"
    checkStatus: "确认状态"
    messageContent: {
      id: ""
      createdAt: "创建时间"
      content: "内容"
    }
  }
}
```
- ***Graphql***

  - body 

  ```text
  {"query":"query{\n  message(id: \"cjveo63w2006p078073k9up6j\") {\n    id\n    toUser\n    sendAt\n    checkedAt\n    checkStatus\n    messageContent{\n      id\n      createdAt\n      fromUser\n      toUser\n      content\n    }\n  }\n}","variables":null}
  ```
- ***Http***

  - body
    ```text
    query{
      message(id: "cjveo63w2006p078073k9up6j") {
        id
        toUser
        sendAt
        checkedAt
        checkStatus
        messageContent{
          id
          createdAt
          fromUser
          toUser
          content
        }
      }
    }
    ```
    
  - response

    ```json
    {
      "data": {
        "message": {
          "id": "cjveo63w2006p078073k9up6j",
          "toUser": "cjvenwfgf00170780jh489frg",
          "sendAt": "2019-05-06T03:34:41.477Z",
          "checkedAt": "2019-05-07T00:31:42.107Z",
          "checkStatus": 1,
          "messageContent": {
            "id": "cjveo6m8s007007809mhjxuie",
            "createdAt": "2019-05-08T03:35:16.252Z",
            "fromUser": "\"cjvet3hsr00900780bcvgthdm\"",
            "toUser": "\"cjvetylgo00f207808gjvsba8\"",
            "content": "内容"
          }
        }
      }
    }
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
  assetses: {
    id: "",
    createdAt: "创建时间",
    publishAddress: "发布地址",
    assetsName: "资产名",
    assetsSymbol: "资产符号",
    decimals: "小数位数",
    totalSupply: "总发送量",
    publishStatus: "发送状态",
  }
```
- ***Graphql***

  - body 

  ```text
   {
      assets(id: "cjveo5ern00620780iw0qx65k") {
        id
        createdAt
        publishAddress
        assetsName
        assetsSymbol
        decimals
        totalSupply
        publishStatus
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"{\n  assets(id: \"cjveo5ern00620780iw0qx65k\") {\n    id\n    createdAt\n    publishAddress\n    assetsName\n    assetsSymbol\n    decimals\n    totalSupply\n    publishStatus\n  }\n}","variables":null,"operationName":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "assets": {
          "id": "cjveo5ern00620780iw0qx65k",
          "createdAt": "2019-05-08T03:34:19.906Z",
          "publishAddress": "0x6c2b65c525814c68bf26a566b69d56237072d0e0",
          "assetsName": "KCLD",
          "assetsSymbol": "CLD",
          "decimals": 2,
          "totalSupply": "1000000",
          "publishStatus": 1
        }
      }
    }
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
  signupOrLogin: {
    token: "token",
    refreshToken: "更新token",
    expiredDate: "到期时间",
    user: {
      id: "",
      createdAt: "创建时间",
      phoneNumber: "电话号码",
      InviterUserID: "邀请人id",
      CountOfInvitees: "邀请用户数量",
      addresses: {
        id: "",
        addressString: "用户地址",
        nickname: "昵称"
      },
      contacts: {
        id: "",
        addressString: "联系人地址",
        nickname: "昵称"
      },
      certificationStatus: {
        id: "",
        createdAt: "创建时间",
        certType: "证件类型",
        certStatus: "认证状态",
        expiredAt: "失效时间",
        submitAt: "提交时间",
        auditAt: "审核时间",
        submitMark: "提交备注",
        auditMark: "审核备注",
        personalCertificationInfo: {
          id: "",
          email: "认证邮箱",
          img1URL: "身份证背面图片url",
          img2URL: "身份证正面图片url",
          identityCardInfo: {
            id: "",
            clientIDNo: "身份证号",
            name: "姓名",
            sex: "性别",
            ethnicity: "民族",
            birth: "出生日期",
            residentialAddress: "居住地",
            authority: "",
            issueDate: "签发日期",
            invalidDate: "无效日期"
          }
        },
        companyCertificationInfo: {
          id: "",
          contacter: "联系人",
          phoneNumberOfContacter: "联系人手机号",
          email: "认证邮箱",
          additionalAuthentication: "附加认证",
          accountName: "银行开户名",
          corporateAccountOfDepositBank: "对公账户开户行",
          corporateAccountNo: "对公账户账号",
          img1URL: "营业执照图片url",
          img2URL: "身份证背面图片url",
          img3URL: "身份证正面图片url",
          identityCardInfo: {
            id: "",
            clientIDNo: "身份证号",
            name: "姓名",
            sex: "性别",
            ethnicity: "民族",
            birth: "出生日期",
            residentialAddress: "居住地",
            authority: "",
            issueDate: "签发日期",
            invalidDate: "无效日期"
          },
          bussinessLicenseInfo: {
            id: "",
            registrationNo: "证件编号",
            unifiedSocialCreditCode: "统一社会信用代码",
            enterpriseName: "名称",
            typeOfEnterprise: "类型",
            residence: "住所",
            legalRepresentative: "法定代表人",
            registeredCapital: "注册资本",
            dateOfEstablishment: "成立日期",
            termOfBusiness: "营业期限",
            scopeOfBusiness: "经营范围"
          }
        }
      },
      certificationRewards: {
        id: "",
        createdAt: "创建时间",
        toAddress: "发送奖励地址",
        receivedAt: "接收奖励地址",
        expiredAt: "到期时间",
        txHash: "交易hash",
        rewardStatus: "奖励状态",
        rewardContent: "奖励内容",
      },
      invitionRewards: {
        id: "",
        createdAt: "创建时间",
        toAddress: "发送奖励地址",
        receivedAt: "接受奖励地址",
        expiredAt: "到期时间",
        txHash: "交易hash",
        inviteeUserID: "受邀者",
        rewardStatus: "奖励状态",
        rewardContent: "奖励内容"
      },
      assetses: {
        id: "",
        createdAt: "创建时间",
        publishAddress: "发布地址",
        assetsName: "资产名",
        assetsSymbol: "资产符号",
        decimals: "小数位数",
        totalSupply: "总发送量",
        publishStatus: "发送状态",
      }
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
