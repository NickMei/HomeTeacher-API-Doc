#reauth 
#### Description
重新认证
#####在个人中心--设置中--修改登陆密码或者修改绑定手机时使用
##### uid checksum要使用登陆态后的值， 不要用 0 和‘0’

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
| password    | String | YES |  | md5(password) |
示例： {'password': 'asccfsdfr35trgfdsg4554'}

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Auth Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/auth/reauth" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "成功认证",
    response: {
        token: "d57c8ab7e18df9cd261892ba81578c8ccbea3f02",
        token_timestamp: "1445223717"
    }
}

其他错误响应情况
{
    retcode: 1, 
    retmsg: "验证密码错误",
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



