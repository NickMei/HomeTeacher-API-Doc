#getStudenCommentList
#### Description
学生个人中心请求学生对老师的评价列表

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


#### Request Parameters (Body) 

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| comment_type | STRING | YES | -- | comment_all（全部） comment_good（好评）  comment_middle（中评）   comment_bad（差评） |
####  示例程序：
#####  {"comment_type":"comment_all"}



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/studentcenter/getStudentCommentList" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "count" :  1, //满足条件总个数
        "list" :  [
            {
                "head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/6.jpg",
                "name": "陈大文",    
                "order_id" : "1",  
                "student_comment": "老师很好！",
                "student_rating": "4",
                "type": "好评"
            }
        ]
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



