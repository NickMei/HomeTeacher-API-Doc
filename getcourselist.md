# getCourseList

#### Description
get course list such as:  全部 器乐 声乐 舞蹈 美术 书法 其它

#### 请求是否要认证
NO

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


#### Request Parameters (Body) JSON

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| stage_id | int | YES |  | 阶段ID |

####  示例程序（JSON）：
#####   var query_obj = {'stage_id': 10};



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/course/getCourseList" |
| --| -- |


#### Response Example

```
{
    "retcode": 0,
    "retmsg": "请求成功！",
    "response": {
        "course_list": [
            {
                "course_id": "93",
                "stage_id": "10",
                "course_name": "全部",
                "priority": "1"
            },
            {
                "course_id": "94",
                "stage_id": "10",
                "course_name": "器乐",
                "priority": "0"
            },
            {
                "course_id": "95",
                "stage_id": "10",
                "course_name": "声乐",
                "priority": "0"
            },
            {
                "course_id": "96",
                "stage_id": "10",
                "course_name": "舞蹈",
                "priority": "0"
            },
            {
                "course_id": "97",
                "stage_id": "10",
                "course_name": "美术",
                "priority": "0"
            },
            {
                "course_id": "98",
                "stage_id": "10",
                "course_name": "书法",
                "priority": "0"
            },
            {
                "course_id": "99",
                "stage_id": "10",
                "course_name": "其它",
                "priority": "0"
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
```






