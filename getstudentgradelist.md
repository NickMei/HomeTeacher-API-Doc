#getStudentGradeList
#### Description
请求学生年级列表

#### 请求是否要认证
NO

#### Resquet Method
POST

#### Request Header 请求头中传的参数
无

#### Request Parameters (Body) 
无


#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/studentcenter/getStudentGradeList" |
| --| -- |
| | |

#### Response Example

#####只有retcode 为0 才是成功响应，其他都是错误响应
```
{
    "retcode": 0,
    "retmsg": "请求成功！",
    "response": {
        "grade_list": [
            "小学一年级",
            "小学二年级",
            "小学三年级",
            "小学四年级",
            "小学五年级",
            "小学六年级",
            "初中一年级",
            "初中二年级",
            "初中三年级",
            "高中一年级",
            "高中二年级",
            "高中三年级"
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



