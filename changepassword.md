#modifyPassword 
#### Description
1. 个人中心--设置--修改个人登录密码   change_password  登录态下需要checksum认证
2. 未登录--寻回个人登录密码  reset_password 无登录态不需要checksum认证


#### 请求是否要认证
1. YES  2. NO

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

####目标：修改密码change_password
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| target    | String | YES |  | 目标：修改密码（change_password）或者 重置密码（reset_password） |
| old_password    | String | YES |  | 现有密码 md5(password) |
| new_password    | String | YES |  | 新密码 md5(password) |
示例： 
######password是md5之后的值
{"target":"change_password", "old_password": "250cf8b51c773f3f8dc8b4be867a9a02", "new_password": "202cb962ac59075b964b07152d234b70"}


####目标：修改密码reset_password
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| target    | String | YES |  | 目标：修改密码（change_password）或者 重置密码（reset_password） |
| new_password    | String | YES |  | 新密码 md5(password) |
| token    | String | YES |  | 第一步成功认证手机号码之后服务器返回的 |
示例： 
######password是md5之后的值
{"target":"reset_password","mobile":"789","new_password":"202cb962ac59075b964b07152d234b70","token":"58180729967baff51d8934bf28d05c4b7394cb1b"}

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Auth Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/auth/modifyPassword" |
| --| -- |
| | |

#### Response Example
##### 需要用返回的token和token_timestamp刷新客户端登录态

#####只有retcode 为0 才是成功响应，其他都是错误响应
####目标：修改密码change_password
```
{
    retcode: 0, 
    retmsg: "修改密码成功 ",
    response: {
        token: "d57c8ab7e18df9cd261892ba81578c8ccbea3f02",
        token_timestamp: "1445223717"
    }
}

其它错误响应
{
    retcode: 1, 
    retmsg: "验证旧有密码错误",
    response: {
    }
}

{
    retcode: 1, 
    retmsg: "更改密码错误",
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


####目标：修改密码reset_password
```
{
    retcode: 0, 
    retmsg: "重置密码成功",
    response: {}
}

{
    retcode: 1, 
    retmsg: "重置密码失败，请重试",
    response: {}
}
```



```



