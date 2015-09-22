#getCommentList
#### Description
学生个人中心请求该学生对所有老师作出的的评价列表(需要验证)

教师详情页请求学生对该老师的评价列表(不需要验证)
#### 请求是否要认证
一个要一个不要

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
| target | STRING | YES | -- | student(该学生作出的评论)  tutor(该教师得到的评论) |
| comment_type | STRING | YES | -- | comment_all（全部） comment_good（好评）  comment_middle（中评）   comment_bad（差评） |




#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/studentcenter/getCommentList" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
1) 获取学员作出的的评论， 要验证
request header:
POST http://112.74.81.48/zhihuieducation/studentcenter/getCommentList HTTP/1.1
uid: 3
identity: student
checksum: a5981159ab5101f244972c8387c529f7

request body:
{"target": "student",  "comment_type": "comment_all"}

response
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "count" :  1, //满足条件总个数
        "list" :  [
            {
                "comment_type": "好评",
                "create_time": "2015-04-09 08:32:42",
                "order_id" : "1", 
                "student_comment": "老师很好！",
                "student_rating": "4",
                "tutor_head_photo": "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/6.jpg",
                "tutor_name": "陈大文",    
            }
        ]
    }
}

2) 获取教员的评论， 不需验证
request header
POST http://112.74.81.48/zhihuieducation/studentcenter/getCommentList HTTP/1.1

request body
{"target": "tutor", "tutor_id": "1",  "comment_type": "comment_all"}

response
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "count" :  1, //满足条件总个数
        "total_rating": 4.5,
        "list" :  [
            {
                comment_type: "好评",
                create_time: "2015-04-09 08:32:42",
                order_id: 1,
                student_comment: "老师很好！",
                student_head_photo: "http://112.74.81.48/zhihuieducation/webApp/app/res/tutor_photo/gd3.jpg",
                student_name: "梅由之",
                student_rating: 4,
                teach_way: "老师上门"
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



