# getCommentAverage

#### Description
教师详情页获取学生对该老师的评价参数(不需要验证)

#### 请求是否要认证
不需要

#### Resquet Method
POST

#### Request Parameters (Body) 

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id | INT | YES | -- |  |

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/studentcenter/getCommentAverage" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
 获取教员的评论参数， 不需验证
request header
POST http://112.74.81.48/zhihuieducation/studentcenter/getCommentAverage

request body
{"tutor_id": "1"}

response
{
    retcode: 0, 
    retmsg: "成功请求！",
    response: {
        "count" :  1, //满足条件总个数
        "total_average_rating": 4.5,
        "knowledge_average_rating": 4.5,
        "attitude_average_rating": 4.5,
        "method_average_rating": 4.5,
    }
}


其他错误响应情况

{
    retcode: 1, 
    retmsg: "错误",
    response: {
    }
}


```



