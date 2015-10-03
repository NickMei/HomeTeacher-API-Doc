#registerAccount 
#### Description
个人中心--注册--设置个人登录密码并且生成注册账号


#### 请求是否要认证
NO

#### Resquet Method
POST


#### Request Parameters (Body)

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| identity    | String | YES | YES | 注册第二步选择的身份 student或者tutor |
| mobile    | String | YES | YES | 注册第一步已经验证过的手机号 |
| password    | String | YES |  | 登陆密码 md5(password) |
| token    | String | YES |  | 第一步成功认证手机号码之后服务器返回的 |
示例： 
######password是md5之后的值
{"identity": "tutor", "mobile": "18682200760", "password":"202cb962ac59075b964b07152d234b70",  "token": "a1910293add748a53092f7b2e778d9100d79a719"}

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Auth Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/auth/registerAccount" |
| --| -- |
| | |

#### Response Example


#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "注册账号18682200760成功",
    response: {}
}

其他错误响应情况
{
    retcode: 1, 
    retmsg: "注册账号18682200760失败，请重新尝试",
    response: {
    }
}

{
    retcode: 1, 
    retmsg: "手机号码认证码错误，请重新验证手机",
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





