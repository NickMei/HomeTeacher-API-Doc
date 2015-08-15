# bookmarkTutor
学员收藏或者取消收藏教员

#### Description
1. 用户没有登录的情况下不能收藏教员
2. 收藏和取消收藏都使用这个API，is_bookmarked

#### Resquet Method
GET
#### Request Parameters

#####
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id | INT | YES | -- |  |
| student_id | INT | YES | -- |  |
| is_bookmarked | INT | YES | -- | 1 收藏教员 或者 0 取消收藏教员 |




#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| |   |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/apitutorinfocontroller/bookmarkTutor?tutor_id=1&student_id=2&is_bookmarked=1" |
| --| -- |


#### Response Example

```
{
    "retcode": 0,
    "retmsg": "操作成功！",
    "result": true
}
```






