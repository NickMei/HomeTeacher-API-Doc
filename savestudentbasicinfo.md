#saveStudentBasicInfo
#### Description
学生个人中心保存我的资料

#### 请求是否要认证
YES

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


#### Request Parameters (Body) 空对象

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| name | varchar | YES | -- | 学生姓名 |
| gender | varchar | YES | -- | 性别 男或女 |
| grade | varchar | YES | -- | 年级 |
| city | varchar | YES | -- | 城市 |
| address | varchar | YES | -- | 地址 |
| self_intro | varchar | YES | -- | 学生个人情况介绍 |
####  示例程序（JSON String）：
#####   {"name":"梅同学","nickname":"小梅","gender":"男","grade":"高中一年级","city":"深圳","address":"深圳市盐田区沿湖路"}



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| |  Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/studentcenter/saveStudentBasicInfo" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "您的信息保存成功！",
    response: {}
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



