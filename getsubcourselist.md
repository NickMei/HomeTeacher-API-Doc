# getSubCourseList


#### Description
get sub course list such as:  全部 芭蕾舞 拉丁舞 街舞 现代舞 爵士舞 古典舞 民族舞 健美操 民间舞 国标舞 迪斯科 其它
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
| course_id | int | YES |  | 课程ID |

####  示例程序（JSON）：
#####   var query_obj = {'course_id': 16};



#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/course/getSubCourseList" |
| --| -- |


#### Response Example

```
{
    "retcode": 0,
    "retmsg": "请求成功！",
    "response": {
            "sub_course_list": [
        {
            "course_sub_id": "35",
            "course_id": "96",
            "course_sub_name": "全部",
            "priority": "1"
        },
        {
            "course_sub_id": "36",
            "course_id": "96",
            "course_sub_name": "芭蕾舞",
            "priority": "0"
        },
        {
            "course_sub_id": "37",
            "course_id": "96",
            "course_sub_name": "拉丁舞",
            "priority": "0"
        },
        {
            "course_sub_id": "38",
            "course_id": "96",
            "course_sub_name": "街舞",
            "priority": "0"
        },
        {
            "course_sub_id": "39",
            "course_id": "96",
            "course_sub_name": "现代舞",
            "priority": "0"
        },
        {
            "course_sub_id": "40",
            "course_id": "96",
            "course_sub_name": "爵士舞",
            "priority": "0"
        },
        {
            "course_sub_id": "41",
            "course_id": "96",
            "course_sub_name": "古典舞",
            "priority": "0"
        },
        {
            "course_sub_id": "42",
            "course_id": "96",
            "course_sub_name": "民族舞",
            "priority": "0"
        },
        {
            "course_sub_id": "43",
            "course_id": "96",
            "course_sub_name": "健美操",
            "priority": "0"
        },
        {
            "course_sub_id": "44",
            "course_id": "96",
            "course_sub_name": "民间舞",
            "priority": "0"
        },
        {
            "course_sub_id": "45",
            "course_id": "96",
            "course_sub_name": "国标舞",
            "priority": "0"
        },
        {
            "course_sub_id": "46",
            "course_id": "96",
            "course_sub_name": "迪斯科",
            "priority": "0"
        },
        {
            "course_sub_id": "47",
            "course_id": "96",
            "course_sub_name": "其它",
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








