#getStudentBasicInfo
#### Description
学生个人中心请求我的资料
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
####  示例程序（空对象）：
#####   var query_obj = {};
#####   var json_str = JSON.stringify(query_obj);


#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Logout Response | JSON | YES| | Logout Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/apistudentcentercontroller/getStudentBasicInfo" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "total_class_time":"6", //学生总学时
        "total_tutor":"2", //学生总的老师数量
        "total_comment":"2" //学生对老师作出的评价数量 
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



