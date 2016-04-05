# getOrderTutorInfo
#### Description
订单确认页


#### 请求是否要登录
YES

#### Resquet Method
POST 



#### Request Parameters (Body)

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id    | int |  |  | 教员ID |
示例： 
{"tutor_id": "1"}

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/order/getOrderTutorInfo" |
| --| -- |
| | |

#### Response Example


#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg："成功提交建议",
    response: {
      'student_info': //学生相关信息
      'teach_info'：//授课相关信息
      'tutor_info': //教员相关信息
    }
}

其他错误响应情况
{
    retcode: 1, 
    retmsg: "提交建议错误",
    response: {
    }
}

```





