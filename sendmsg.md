#sendMsg 
#### Description
个人中心--设置--发送验证码到新手机号码

##### uid和checksum要使用登陆态后的值， 不要用 0 和‘0’

#### 请求是否要认证
YES

#### Resquet Method
POST


#### Request Header 请求头中传的参数
######uid没有登陆情况下为整形integer零 0， 登陆成功后会返回user_id
######identity 根据用户选择的身份，student 或者 tutor
######checksum由三个步骤算出，参考下面图片JS代码和注释，包含token安全验证以及post数据完整性校验功能

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| uid | int | YES |  | 0 |
| identity    | String | YES |  | tutor 或者 student|
| checksum    | String | YES |  | checksum|


#### Request Parameters (Body)

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| target    | String | YES |  | 请求目的，change_mobile, register |
| mobile    | String | YES |  | 需要绑定的新手机号码 |

示例： 
{"target":"change_mobile", "mobile": "13609876789"}

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Auth Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/auth/sendMsg" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg："请求成功！",
    response: {
        msgcode: "120708" //仅供调试使用，上线后手机收短信验证码
    }
}

其他错误响应情况
{
    retcode: 1, 
    retmsg: "错误！",
    response: {
    }
}


可能是丢失数据，或者token无效或者过期，提示用户重新登陆
{
    retcode: 2, 
    retmsg: "验证无法通过，请重新登陆",
    response: {
    }
}
```



