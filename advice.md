#advice 
#### Description
个人中心--帮助中心--意见反馈


#### 请求是否要认证
NO

#### Resquet Method
POST 



#### Request Parameters (Body)

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| mobile    | String | YES |  | 反馈留的手机号码 |
| advice_content    | String | YES |  | 反馈内容 |
示例： 
{"mobile": "13609876789", "advice_content": "期待开通广州"}

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Auth Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/helpcenter/advice" |
| --| -- |
| | |

#### Response Example


#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg："成功提交建议",
    response: {
    }
}

其他错误响应情况
{
    retcode: 1, 
    retmsg: "提交建议错误",
    response: {
    }
}

```



