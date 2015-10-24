# getStageList

#### Description
get stage list such as:  小学 小升初 初中 中考 高中 高考 大学 语言 留学 艺术 体育 心理

#### 请求是否要认证
NO

#### Resquet Method
GET
#### Request Parameters

| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |




#### Response
| Name | Type | Mandatory | Default | Description |
| -- | -- | -- | -- | -- |
| Response | JSON | YES| | Response |


#### Request Example

|Request URL | "http://112.74.81.48/zhihuieducation/course/getStageList" |
| --| -- |


#### Response Example

```
{
    "retcode": 0,
    "retmsg": "请求成功！",
    "response": {
        "stage_list": [
    {
        "stage_id": "13",
        "stage": "全部",
        "priority": "1"
    },
    {
        "stage_id": "1",
        "stage": "小学",
        "priority": "0"
    },
    {
        "stage_id": "2",
        "stage": "小升初",
        "priority": "0"
    },
    {
        "stage_id": "3",
        "stage": "初中",
        "priority": "0"
    },
    {
        "stage_id": "4",
        "stage": "中考",
        "priority": "0"
    },
    {
        "stage_id": "5",
        "stage": "高中",
        "priority": "0"
    },
    {
        "stage_id": "6",
        "stage": "高考",
        "priority": "0"
    },
    {
        "stage_id": "7",
        "stage": "大学",
        "priority": "0"
    },
    {
        "stage_id": "8",
        "stage": "语言",
        "priority": "0"
    },
    {
        "stage_id": "9",
        "stage": "留学",
        "priority": "0"
    },
    {
        "stage_id": "10",
        "stage": "艺术",
        "priority": "0"
    },
    {
        "stage_id": "11",
        "stage": "体育",
        "priority": "0"
    },
    {
        "stage_id": "12",
        "stage": "心理",
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






