#logout 
#### Description
登出
#### Resquet Method
POST


#### Request Header 请求头中传的参数
######uid没有登陆情况下为整形integer零 0， 登陆成功后使用user_id
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
####  实例程序（空对象）：
#####   var query_obj = {};
#####   var json_str = JSON.stringify(query_obj);

#####说明：服务器端会用请求体中传来的数据和 服务器存的token request_str 计算checksum，再和请求头中的checksum比较。

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Logout Response | JSON | YES| | Logout Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/auth/logout" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "成功登出！",
    response: {
    }
}

其他错误响应情况

{
    retcode: 1, 
    retmsg: "错误",
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



