# addOrder

#### Description
提交订单


#### 请求是否要登录
YES

#### Resquet Method
POST 



#### Request Parameters (Body)

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id    | int |  |  | 教员ID |
| student_id    | int |  |  | 学员ID |
| course_id    | int |  |  | 课程ID |
| way_id    | int |  |  | 授课方式 |
| price    | int |  |  | 价格 |
| class_address    | varchar |  |  | 上课地址 |
| student_name    | varchar |  |  | 学员姓名 |
| extra_info    | varchar |  |  | 额外信息 |
| class_time    | varchar |  |  | 上课时间 |
示例： 
{{"tutor_id":"14","student_id":"1","course_id":"1","way_id":"1","price":"150","class_address":"深圳市盐田区沿湖路","student_name":"罗同学","extra_info":"XXX","class_time":"周一"}:}

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Auth Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/order/addOrder" |
| --| -- |
| | |

#### Response Example


#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    retcode: 0, 
    retmsg："成功",
    response: {
      'result': 1

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






