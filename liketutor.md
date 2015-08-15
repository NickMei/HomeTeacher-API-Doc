# likeTutor
赞教员 或者 取消赞教员

#### Description
1. 用户没有登录的情况下不能赞教员
2. 赞和取消赞都使用这个API，is_liked区分

#### Resquet Method
GET
#### Request Parameters

#####
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id | INT | YES | -- |  |
| student_id | INT | YES | -- |  |
| is_liked | INT | YES | -- | 1 赞 或者 0 取消赞 |




#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| |   |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/apitutorinfocontroller/likeTutor?tutor_id=1&student_id=2&is_liked=1" |
| --| -- |


#### Response Example

```
{
    "retcode": 0,
    "retmsg": "操作成功！",
    "result": true
}
```






