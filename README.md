## Grampus wallet App API documnet

`url: http://119.3.43.136:8080/query`

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
###  Q1-8.查询交易记录(全部、单条)

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
    {
      tradingRecords(tradingAddress: "0x349118dD4764b6335055582949a24A1d76DDad15", contractAddress: "0x349118dD4764b6335055582949a24A1d76DDad15", limit: 10, skip: 0) {
        txHash
        createdAt
        blockNumber
        tradingType
        tradingStatus
        amount
        from
        to
        contractAddress
        contractSymbol
        comment
      }
    }
  ```
- ***Http***

  - parameter
  `tradingAddress: 鲸卡，contractAddress：资产，limit： 分页条数， skip：从第几条开始 (limit必须跟skip同时传)，不传参数是全部`

  - body
    ```text
    {"query":"{\n  tradingRecords(tradingAddress: \"0x349118dD4764b6335055582949a24A1d76DDad15\", contractAddress: \"0x349118dD4764b6335055582949a24A1d76DDad15\", limit: 10, skip: 0) {\n    txHash\n    createdAt\n    blockNumber\n    tradingType\n    tradingStatus\n    amount\n    from\n    to\n    contractAddress\n    contractSymbol\n    comment\n  }\n}\n","variables":null,"operationName":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "tradingRecords": [
          {
            "txHash": "0xed2b8aba29dda5076dd40e5f0f9e8fafccd505472e3b096afb918af65bec1256",
            "createdAt": "1557935063",
            "blockNumber": 0,
            "tradingType": 1,
            "tradingStatus": 2,
            "amount": "10005",
            "from": "0x349118dD4764b6335055582949a24A1d76DDad15",
            "to": "0x14CA04Ff85747DEF87d6c6C566dB84Cc24e4643b",
            "contractAddress": "",
            "contractSymbol": "",
            "comment": ""
          }
        ]
      }
    }
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
    toUserID: "消息接受者"
    sendAt: "发送时间"
    checkedAt: "确认时间"
    checkStatus: "确认状态"
    messageContent: {
      id: ""
      createdAt: "创建时间"
      content: "内容"
      title: "标题"
      fromUserID: "消息发送者"
    }
  }
}
```
- ***Graphql***

  - body 

  ```text
    {
      messages(limit:10,skip:0){
        id
        sendAt
        checkedAt
        checkStatus
        toUserID
        messageContent {
          id
          createdAt
          title
          content
          fromUserID
        }
      }
    }


  ```
- ***Http***

  - parameter
    ```text
    limit: 查询条数, skip: 从第几条开始查
    ```

  - body
    ```text
    {"query":"{\n  messages(limit:10,skip:0){\n    id\n    sendAt\n    checkedAt\n    checkStatus\n    toUserID\n    messageContent {\n      id\n      createdAt\n      title\n      content\n      fromUserID\n    }\n  }\n}\n","variables":null,"operationName":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "messages": [
          {
            "id": "cjvltwrhh009e0791qim6w8yq",
            "sendAt": "1557546582",
            "checkedAt": null,
            "checkStatus": 0,
            "toUserID": "cjvls5tmq001b0791gkdkucvq",
            "messageContent": {
              "id": "cjvltwb5m00910791c6ikmtqw",
              "createdAt": "1557719376",
              "title": "系统消息",
              "content": "消息内容",
              "fromUserID": "cjvls62u7001l0791ffq9jvwl"
            }
          },
          {
            "id": "cjvonjdvs02pa0791in8mvx7w",
            "sendAt": "1557717268",
            "checkedAt": null,
            "checkStatus": 0,
            "toUserID": "cjvls5tmq001b0791gkdkucvq",
            "messageContent": {
              "id": "cjvltwb5m00910791c6ikmtqw",
              "createdAt": "1557719376",
              "title": "系统消息",
              "content": "消息内容",
              "fromUserID": "cjvls62u7001l0791ffq9jvwl"
            }
          },
          {
            "id": "cjvonjw3902pu0791h263ko9t",
            "sendAt": "1557717302",
            "checkedAt": "1557803706",
            "checkStatus": 1,
            "toUserID": "cjvls5tmq001b0791gkdkucvq",
            "messageContent": {
              "id": "cjvltwb5m00910791c6ikmtqw",
              "createdAt": "1557719376",
              "title": "系统消息",
              "content": "消息内容",
              "fromUserID": "cjvls62u7001l0791ffq9jvwl"
            }
          },
          {
            "id": "cjvonk9ou02q70791zexf7kr4",
            "sendAt": "1557026121",
            "checkedAt": null,
            "checkStatus": 0,
            "toUserID": "cjvls5tmq001b0791gkdkucvq",
            "messageContent": {
              "id": "cjvltwb5m00910791c6ikmtqw",
              "createdAt": "1557719376",
              "title": "系统消息",
              "content": "消息内容",
              "fromUserID": "cjvls62u7001l0791ffq9jvwl"
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
   {
      message(id: "cjvltwrhh009e0791qim6w8yq") {
        id
        sendAt
        checkedAt
        checkStatus
        toUserID
        messageContent{
          id
          createdAt
          title
          content
          fromUserID
        }
      }
    }
  ```
- ***Http***

  - parameter
    ```text
    id: messageID
    ```

  - body
    ```text
    {"query":"{\n  message(id: \"cjvltwrhh009e0791qim6w8yq\") {\n    id\n    sendAt\n    checkedAt\n    checkStatus\n    toUserID\n    messageContent{\n      id\n      createdAt\n      title\n      content\n      fromUserID\n    }\n  }\n}\n","variables":null,"operationName":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "message": {
          "id": "cjvltwrhh009e0791qim6w8yq",
          "sendAt": "1557546582",
          "checkedAt": null,
          "checkStatus": 0,
          "toUserID": "cjvls5tmq001b0791gkdkucvq",
          "messageContent": {
            "id": "cjvltwb5m00910791c6ikmtqw",
            "createdAt": "1557719376",
            "title": "系统消息",
            "content": "消息内容",
            "fromUserID": "cjvls62u7001l0791ffq9jvwl"
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
    {
      erc20s(key: ""){
        address
        blockNumber
        name
        totalSupply
        decimals
        symbol
      }
    }
  ```
- ***Http***

  - paramter
  `key 是address,name,symbol的模糊查询，空是全部`

  - body
    ```text
    {"query":"{\n  erc20s(key: \"\"){\n    address\n    blockNumber\n    name\n    totalSupply\n    decimals\n    symbol\n  }\n}\n","variables":null,"operationName":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "erc20s": [
          {
            "address": "0x8CD65D4Bffe7F3638690047fb2ab3B9E52f8a31d",
            "blockNumber": 344510,
            "name": "LPS",
            "totalSupply": "1000000",
            "decimals": 2,
            "symbol": "LPC"
          },
          {
            "address": "0xCadb671eAd6aaB7B198fB04296dC928393Bb050D",
            "blockNumber": 344510,
            "name": "KDJDsd",
            "totalSupply": "1000000",
            "decimals": 2,
            "symbol": "DFGD"
          },
          {
            "address": "0xAAa53c53Bb35F93D68bdd6C6942DddaFCCcf8a59",
            "blockNumber": 346620,
            "name": "LLDJ",
            "totalSupply": "1000000",
            "decimals": 2,
            "symbol": "DJ"
          }
        ]
      }
    }
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

  - parameter
    ```text
    id: assetsID
    ```

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
    mutation{
      sendVerificationCode(phoneNumber: "17740657205") { 
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  sendVerificationCode(phoneNumber: \"17740657205\") { \n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "sendVerificationCode": true
      }
    }
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
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  signupOrLogin(phoneNumber: \"18721341306\", verificationCode: \"1234\", inviteCode: \"\") {\n    token\n    refreshToken\n    expiredDate\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "signupOrLogin": {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0xM1QwMzowMTowMC44NTBaIiwiZXhwIjoxNTk3NzI2NjMwLCJpZCI6IlkycDJiSE0xZEcxeE1EQXhZakEzT1RGbmEyUnJkV04yY1E9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQifQ.EnMRmquCtmkot6_3Cqe3RycD56IJuqajCBdJGyzmc60",
          "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0xM1QwMzowMTowMC44NTBaIiwiZXhwIjoyMzU3NzI2NjMwLCJpZCI6IlkycDJiSE0xZEcxeE1EQXhZakEzT1RGbmEyUnJkV04yY1E9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQiLCJvbmx5X3JlZnJlc2giOiJ0cnVlIn0.9BnQkz9piel1KECchlCtfKtZq0-T9vgJ2TvyBhmkp9Y",
          "expiredDate": "1597726630"
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
  mutation{
     refreshToken(refreshToken: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0wOFQwMzoyNzoyMC44NzhaIiwiZXhwIjoxNTU4NjAzMTg4LCJpZCI6IlkycDJaVzUzWm1kbU1EQXhOekEzT0RCcWFEUTRPV1p5Wnc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQiLCJvbmx5X3JlZnJlc2giOiJ0cnVlIn0.R0zC7IgHNw9UPZYpkjzHEyrekRlB1cO602tvKZppbjY") {
      token
      expiredDate
      refreshToken
    }
  }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n refreshToken(refreshToken: \"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiMjAxOS0wNS0wOFQwMzoyNzoyMC44NzhaIiwiZXhwIjoxNTU4NjAzMTg4LCJpZCI6IlkycDJaVzUzWm1kbU1EQXhOekEzT0RCcWFEUTRPV1p5Wnc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQiLCJvbmx5X3JlZnJlc2giOiJ0cnVlIn0.R0zC7IgHNw9UPZYpkjzHEyrekRlB1cO602tvKZppbjY\") {\n  token\n  expiredDate\n  refreshToken\n}\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "refreshToken": {
          "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiIiwiZXhwIjoxNTU3ODQzMjE1LCJpZCI6IlkycDJaVzUzWm1kbU1EQXhOekEzT0RCcWFEUTRPV1p5Wnc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQifQ.jctSRXp9jZwNBJeo3MiqgPV4DKi8iHAKSfTSVuxpTtU",
          "expiredDate": "1557843215",
          "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVkX2F0IjoiIiwiZXhwIjoxNTU4NjAzMjE1LCJpZCI6IlkycDJaVzUzWm1kbU1EQXhOekEzT0RCcWFEUTRPV1p5Wnc9PSIsImlzcyI6ImdyYW1wdXMtYXNzZXRzLWJhY2tlbmQiLCJvbmx5X3JlZnJlc2giOiJ0cnVlIn0.Ct-DcEYirLBNNy6GXrdvvzyHAiCtCTpl2HXJxjDFLD8"
        }
      }
    }
    ```
###  M1-4.添加鲸卡

- ***API***

```text
mutation->addAddress
```
- ***Describe***

```text
addAddress{
    id: ""
    addressString: "添加鲸卡地址",
    nickname: "添加鲸卡昵称"
}
```
- ***Graphql***

  - body 

  ```text
    mutation{
     addAddress(address: "0x14ca04ff85747def87d6c6c566db84cc24e4643b", nickname: "JK新卡") {
      id
      addressString
      nickname
     } 
    }
  ```
- ***Http***

  - parameter
    ```text
    address: 地址, nickname: 昵称
    ```

  - body
    ```text
    {"query":"mutation {\n  addAddress(address: \"0x14ca04ff85747def87d6c6c566db84cc24e4643b\", nickname: \"JK新卡\") {\n    id\n    addressString\n    nickname\n  }\n}\n","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "addAddress": {
          "id": "cjvnlkb1q02000791y22thhe9",
          "addressString": "0x14ca04ff85747def87d6c6c566db84cc24e4643b",
          "nickname": "JK新卡"
        }
      }
    }
    ```
###  M1-5.修改鲸卡昵称

- ***API***

```text
mutation->updateAddressNickname
```
- ***Describe***

```text
addAddress{
    id: ""
    addressString: "添加鲸卡地址",
    nickname: "添加鲸卡昵称"
}
```
- ***Graphql***

- parameter
    ```text
    id: 地址id, nickname: 昵称
    ```

  - body 

  ```text
    mutation{
      updateAddressNickname(id: "cjvg2ktv700k40714qdns6al7", nickname: "sad") {
        id
        addressString
        nickname
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  updateAddressNickname(id: \"cjvg2ktv700k40714qdns6al7\", nickname: \"sad\") {\n    id\n    addressString\n    nickname\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "updateAddressNickname": {
          "id": "cjvg2ktv700k40714qdns6al7",
          "addressString": "0xdnjskjndksmkd",
          "nickname": "sad"
        }
      }
    }
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
    mutation{
      deleteAddress(id: "cjvg3a2hg00m00714etpxw3an") {
        id
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  deleteAddress(id: \"cjvg3a2hg00m00714etpxw3an\") {\n    id\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "deleteAddress": {
          "id": "cjvg3a2hg00m00714etpxw3an"
        }
      }
    }
    ```
###  M1-7.添加通讯录名单

- ***API***

```text
mutation->addContacter
```
- ***Describe***

```text
addContacter{
    id: ""
    addressString: "通讯录地址",
    nickname: "通讯录昵称"
}
```
- ***Graphql***

  - body 

  ```text
    mutation{
      addContacter(contacterAddress: "0xsahsja", nickname: "dsd") {
        id
        addressString
        nickname
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  addContacter(contacterAddress: \"0xsahsja\", nickname: \"dsd\") {\n    id\n    addressString\n    nickname\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "addContacter": {
          "id": "cjvg2sb9s00kr0714ohujdaqs",
          "addressString": "0xsahsja",
          "nickname": "dsd"
        }
      }
    }
    ```
###  M1-8.更新通讯录名单

- ***API***

```text
mutation->updateContacter
```
- ***Describe***

```text
addContacter{
    id: ""
    addressString: "通讯录地址",
    nickname: "通讯录昵称"
}
```
- ***Graphql***

  - body 

  ```text
    mutation{
      updateContacter(id: "cjvg2ulgi00ky07144imnt2r2", contacterAddress: "0xsds", nickname: "sddss") {
        id
        addressString
        nickname
      }
    }
  ```
- ***Http***

  - parameter
    ```text
    id: 地址id, nickname: 昵称, contacterAddress: 通讯录地址
    ```

  - body
    ```text
    {"query":"mutation{\n  updateContacter(id: \"cjvg2ulgi00ky07144imnt2r2\", contacterAddress: \"0xsds\", nickname: \"sddss\") {\n    id\n    addressString\n    nickname\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "updateContacter": {
          "id": "cjvg2ulgi00ky07144imnt2r2",
          "addressString": "0xsds",
          "nickname": "sddss"
        }
      }
    }
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
    mutation{
      deleteContacter(id: "cjvg2ulgi00ky07144imnt2r2") {
        id
      }
    }
  ```
- ***Http***

  - parameter
    ```text
    id: 删除id
    ```

  - body
    ```text
    {"query":"mutation{\n  deleteContacter(id: \"cjvg2ulgi00ky07144imnt2r2\") {\n    id\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "deleteContacter": {
          "id": "cjvg2ulgi00ky07144imnt2r2"
        }
      }
    }
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
    mutation {
      personalCertificate(name: "陈朋涛", clientIDNo: "532101198906010015", identityCardFrontInfoID: "cjvnc9wqj00ot07147u5odppf", identityCardBackInfoID: "cjvnckwlq00oy0714lpdqivqy") {
        id
        name
        clientIDNo
        idCardBackImgURL
        idCardFrontImgURL
      }
    }

  ```
- ***Http***

  - body
    ```text
    {"query":"mutation {\n  personalCertificate(name: \"陈朋涛\", clientIDNo: \"532101198906010015\", identityCardFrontInfoID: \"cjvnc9wqj00ot07147u5odppf\", identityCardBackInfoID: \"cjvnckwlq00oy0714lpdqivqy\") {\n    id\n    name\n    clientIDNo\n    idCardBackImgURL\n    idCardFrontImgURL\n  }\n}\n","variables":null}
    ```
    
  - response

    ```json
    {
      "errors": [
        {
          "message": "graphql: panic occurred: runtime error: invalid memory address or nil pointer dereference",
          "path": [
            "personalCertificate"
          ]
        }
      ],
      "data": {
        "personalCertificate": null
      }
    }
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
    mutation{
      prepareTrading(txid: "sss") {
        
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  prepareTrading(txid: \"sss\") {\n    \n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "errors": [
        {
          "message": "graphql: panic occurred: not implemented",
          "path": [
            "prepareTrading"
          ]
        }
      ],
      "data": {
        "prepareTrading": null
      }
    }
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

  - paramter
  `全部已读，不传参数，只读某一条传id`

  - body 

  ```text
    mutation{
      checkMessage() {
    	}
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  checkMessage() {\n\t}\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "checkMessage": 0
      }
    }
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
    mutation{
      receiveCertificationReward(toAddress: "0x941c69B23CeF5f5021b5966f4ba85fE6Bf9A58E1")
    }

  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  receiveCertificationReward(toAddress: \"0x941c69B23CeF5f5021b5966f4ba85fE6Bf9A58E1\")\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "receiveCertificationReward": false
      }
    }
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
    mutation{
      receiveInvitionRewards(toAddress: "0x941c69B23CeF5f5021b5966f4ba85fE6Bf9A58E1")
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  receiveInvitionRewards(toAddress: \"0x941c69B23CeF5f5021b5966f4ba85fE6Bf9A58E1\")\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "receiveInvitionRewards": true
      }
    }
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
    mutation {
      resolveBackOfIdentityCard(img: "img_base64") {
        id
        imgURL
        authority
        issueDate
        invalidDate
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation {\n  resolveBackOfIdentityCard(img: \"img_base64\") {\n    id\n    imgURL\n    authority\n    issueDate\n    invalidDate\n  }\n}\n","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "resolveBackOfIdentityCard": {
          "id": "cjvnckwlq00oy0714lpdqivqy",
          "imgURL": null,
          "authority": "成都市公安局龙泉驿区分局",
          "issueDate": "20110922",
          "invalidDate": "20310922"
        }
      }
    }
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
    mutation {
      resolveFrontOfIdentityCard(img: "img_base64") {
        id
        imgURL
      	clientIDNo
      	ethnicity
      	birth
      	residentialAddress
      	sex
      	name
      }
    }
  ```
- ***Http***

  - paramter
  `img: base64(不要"data:image/jpeg;base64,"这一段)`

  - body
    ```text
    {"query":"mutation {\n  resolveFrontOfIdentityCard(img: \"img_base64\") {\n    id\n    imgURL\n  \tclientIDNo\n  \tethnicity\n  \tbirth\n  \tresidentialAddress\n  \tsex\n  \tname\n  }\n}\n","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "resolveFrontOfIdentityCard": {
          "id": "cjvnc9wqj00ot07147u5odppf",
          "imgURL": null,
          "clientIDNo": "532101198906010015",
          "ethnicity": "汉",
          "birth": "19890601",
          "residentialAddress": "山东省滕州市龙阳镇",
          "sex": "男",
          "name": "陈朋涛"
        }
      }
    }
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
###  M1-26.添加交易记录

- ***API***

```text
mutation->addTradingRecord
```
- ***Describe***

```text

```
- ***Graphql***

  -paramter
  `txHash: web3go发送交易返回的hash，（不能重复，测试的时候改一下），from: 发送地址，to: 接收地址，ammount：金额，comment：备注`

  - body 

  ```text
  mutation{
      addTradingRecord(txHash: "0xed2b8aba29dda5076dd40e5f0f9e8fafccd505472e3b096afb918af65bec25b4", from: "0x14CA04Ff85747DEF87d6c6C566dB84Cc24e4643b", to: "0x349118dD4764b6335055582949a24A1d76DDad15", amount: "1000", comment: "备注") {
        
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"mutation{\n  addTradingRecord(txHash: \"0xed2b8aba29dda5076dd40e5f0f9e8fafccd505472e3b096afb918af65bec25b2\", from: \"0x14CA04Ff85747DEF87d6c6C566dB84Cc24e4643b\", to: \"0x349118dD4764b6335055582949a24A1d76DDad15\", amount: \"1000\", comment: \"备注\") {\n    \n  }\n}\n","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "addTradingRecord": true
      }
    }
    ```
###  P1-1.获取鲸卡信息

- ***API***

```text
query->Q1-1->S2-6
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
    query{
      user{
        addresses{
          id
          addressString
          nickname
        }
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"{\n  user {\n    addresses {\n      id\n      addressString\n      nickname\n    }\n  }\n}\n","variables":null,"operationName":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "user": {
          "addresses": [
            {
              "id": "cjvenwz0i001t0780x1kyh1qc",
              "addressString": "0x349118dd4764b6335055582949a24a1d76ddad15",
              "nickname": "鲸卡2"
            },
            {
              "id": "cjvf0h9rt00ei0714g157pxlk",
              "addressString": "0x14ca04ff85747ccf87d6c6c566db84cc24e4643b",
              "nickname": "鲸卡3"
            },
            {
              "id": "cjvg2ghba00jq0714t3zr6luq",
              "addressString": "0xdnjskjndksmkd",
              "nickname": "dhshb"
            },
            {
              "id": "cjvg2hvul00jx0714tno01u0b",
              "addressString": "0xdnjskjndksmkd",
              "nickname": "dhshb"
            },
            {
              "id": "cjvn7n8im00kk0714698tqcv5",
              "addressString": "0x14ca04ff85747def87d6c6c566db84cc24e4643b",
              "nickname": "JK新卡"
            },
            {
              "id": "cjvn7pe5s00kr07147w54b8ph",
              "addressString": "0x14ca04ff85747def87d6c6c566db84cc24e4643b",
              "nickname": "JK新卡"
            }
          ]
        }
      }
    }
    ```

###  P1-2.获取通讯录

- ***API***

```text
query->Q1-1->S2-7
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
    query{
      user{
        contacts{
          id
          addressString
          nickname
        }
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"query{\n  user{\n    contacts{\n      id\n      addressString\n      nickname\n    }\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "user": {
          "contacts": [
            {
              "id": "cjvenxdld002g07802xry4w4a",
              "addressString": "0x619f889c5699394b9c5033bc85028eb4af11faa1",
              "nickname": "朋友2"
            },
            {
              "id": "cjvf263qy00fd0714f4ron0yy",
              "addressString": "0x14ca04ff85747ccfc4387866db84cc24e4643b",
              "nickname": "好友4"
            },
            {
              "id": "cjvg2sb9s00kr0714ohujdaqs",
              "addressString": "0xsahsja",
              "nickname": "dsd"
            }
          ]
        }
      }
    }
    ```

###  P1-3.获取奖励次数

- ***API***

```text
query->Q1-1->S2-9
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
    query{
      user{
        certificationRewards{
          id
        }
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"query{\n  user{\n    certificationRewards{\n      id\n    }\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "user": {
          "certificationRewards": []
        }
      }
    }
    ```

###  P1-4.获取邀请好友个数

- ***API***

```text
query->Q1-1->S2-5
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
    query{
      user{
        CountOfInvitees
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"query{\n  user{\n    CountOfInvitees\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "user": {
          "CountOfInvitees": 3
        }
      }
    }
    ```

###  P1-5.当前累计奖励

- ***API***

```text
query->Q1-1->S2-10
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
    query{
      user{
        certificationRewards{
          id
          rewardContent{
            rewardPoint
          }
        }
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"query{\n  user{\n    certificationRewards{\n      id\n      rewardContent{\n        rewardPoint\n      }\n    }\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "user": {
          "certificationRewards": []
        }
      }
    }
    ```

###  P1-6.用户手机号，姓名，是否实名，消息数

- ***API***

```text
query->Q1-1->S5-9
```
- ***Describe***

```text

```
- ***Graphql***

  - body 

  ```text
    query{
      user{
        phoneNumber
        certificationStatuses{
          personalCertificationInfo{
            name
          }
          certType
          certStatus
        }
      }
      messages{
        id
        checkStatus
      }
    }
  ```
- ***Http***

  - body
    ```text
    {"query":"query{\n  user{\n    phoneNumber\n    certificationStatuses{\n      personalCertificationInfo{\n        name\n      }\n      certType\n      certStatus\n    }\n  }\n  messages{\n    id\n    checkStatus\n  }\n}","variables":null}
    ```
    
  - response

    ```json
    {
      "data": {
        "user": {
          "phoneNumber": "18721341306",
          "certificationStatuses": [
            {
              "personalCertificationInfo": {
                "name": "张三"
              },
              "certType": 1,
              "certStatus": 1
            }
          ]
        },
        "messages": [
          {
            "id": "cjvltwrhh009e0791qim6w8yq",
            "checkStatus": 0
          },
          {
            "id": "cjvonjdvs02pa0791in8mvx7w",
            "checkStatus": 0
          },
          {
            "id": "cjvonjw3902pu0791h263ko9t",
            "checkStatus": 1
          },
          {
            "id": "cjvonk9ou02q70791zexf7kr4",
            "checkStatus": 0
          }
        ]
      }
    }
    ```
