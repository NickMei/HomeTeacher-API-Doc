# bookmarkTutor
学员收藏或者取消收藏教员

#### Description
1. 用户没有登录的情况下不能收藏教员
2. 收藏和取消收藏都使用这个API，is_bookmarked
 
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
#####
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| tutor_id | INT | YES | -- |  |
| student_id | INT | YES | -- |  |
| is_bookmarked | INT | YES | -- | 1 收藏教员 或者 0 取消收藏教员 |

#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/tutorinfo/bookmarkTutor" |
| --| -- |
{"tutor_id": 1, "student_id": 2, "is_bookmarked": 1}

#### Response Example

```
{
    "retcode": 0,
    "retmsg": "操作成功！",
    "result": true
}
```






